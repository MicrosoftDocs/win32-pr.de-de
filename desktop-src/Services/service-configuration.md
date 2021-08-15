---
description: Das System verwendet die Konfigurationsinformationen, um zu bestimmen, wie der Dienst gestartet wird.
ms.assetid: fc8c631e-076c-4745-8db0-90f46a202e6a
title: Dienstkonfiguration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34f64b5cef835e1c7efef10c12555c81c132e707c8d1fb2814a7fcb95cf6d71c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118889080"
---
# <a name="service-configuration"></a>Dienstkonfiguration

Das System verwendet die Konfigurationsinformationen, um zu bestimmen, wie der Dienst gestartet wird. Die Konfigurationsinformationen enthalten auch den Anzeigenamen des Diensts und dessen Beschreibung. Beispielsweise können Sie für den DHCP-Dienst den Anzeigenamen "Dynamic Host Configuration Protocol Service" und die Beschreibung "Stellt Internetadressen für Computer in Ihrem Netzwerk bereit" verwenden.

Um die Konfigurationsinformationen für ein Dienstobjekt zu ändern, verwendet ein Konfigurationsprogramm die [**Funktion ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) oder [**ChangeServiceConfig2.**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a) Ein Beispiel finden Sie unter [Ändern einer Dienstkonfiguration.](changing-a-service-configuration.md)

Um die Konfigurationsinformationen für ein Dienstobjekt abzurufen, verwendet das Konfigurationsprogramm die [**QueryServiceConfig-**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfiga) oder [**QueryServiceConfig2-Funktion.**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfig2a) Ein Beispiel finden Sie unter [Abfragen der Konfiguration eines Diensts.](querying-a-service-s-configuration.md)

Die Dienstkonfigurationsfunktionen [**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a) und [**QueryServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfig2a) unterstützen die Verwendung von Triggern zum Steuern des Dienststarts.

Um die Sicherheitsbeschreibung für ein SCManager-Objekt oder ein Dienstobjekt zu ändern, verwendet ein Konfigurationsprogramm die [**SetServiceObjectSecurity-Funktion.**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) Um eine Kopie der Sicherheitsbeschreibung abzurufen, verwendet das Konfigurationsprogramm die [**QueryServiceObjectSecurity-Funktion.**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Konfigurieren eines Diensts mit sc](configuring-a-service-using-sc.md)
</dt> </dl>

 

 
