# Architecture Overview

## System Components

### Frontend
- **Framework**: React 18 with TypeScript
- **State Management**: Redux Toolkit
- **UI Library**: Material-UI
- **Canvas Library**: Fabric.js for annotation

### Backend
- **Framework**: FastAPI (Python 3.11+)
- **ORM**: SQLAlchemy
- **Authentication**: JWT tokens
- **Task Queue**: Celery with Redis

### Database
- **Primary**: PostgreSQL 15
- **Cache**: Redis
- **Object Storage**: MinIO (S3-compatible)

### Infrastructure
- **Containerization**: Docker + Docker Compose
- **CI/CD**: GitHub Actions
- **Monitoring**: Prometheus + Grafana

## Data Flow

1. User uploads data files
2. Backend stores files in object storage
3. Annotation tasks created in database
4. Users annotate via interactive canvas
5. Annotations saved incrementally
6. Quality review workflow
7. Export to ML formats (COCO, YOLO, Pascal VOC)
