---
title: Zertifikat Sperrung wird überprüft
description: Zertifikat Sperrung wird überprüft
ms.assetid: 498bd2a5-4336-4fc4-9718-6c5fe2db9066
keywords:
- Windows Media-Format-SDK, DRM-Import
- SDK für Windows Media-Format, importieren
- Windows Media-Format-SDK, Zertifikat Sperrung
- Windows Media-Format-SDK, Sperren von Zertifikaten
- Digital Rights Management (DRM), importieren
- DRM (Digital Rights Management), importieren
- Digital Rights Management (DRM), Zertifikats Sperrung
- DRM (Digital Rights Management), Zertifikats Sperrung
- Digital Rights Management (DRM), Sperren von Zertifikaten
- DRM (Digital Rights Management), Sperren von Zertifikaten
- Erweiterte APIs für den DRM-Client, Import
- Erweiterte Client-APIs, importieren
- Erweiterte APIs für den DRM-Client, Zertifikat Sperrung
- Erweiterte Client-APIs, Zertifikats Sperrung
- Erweiterte APIs für den DRM-Client, Sperren von Zertifikaten
- Erweiterte Client-APIs, Sperren von Zertifikaten
- Zertifikate, Sperren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcbb72dd52870437ef9b69b30cc36a57725abe09
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710235"
---
# <a name="checking-certificate-revocation"></a>Zertifikat Sperrung wird überprüft

Beim Importieren von Inhalten in Windows Media DRM müssen Sie sicherstellen, dass kein Zertifikat in einer Zertifikat Sammlung widerrufen wurde, indem Sie überprüfen, ob in der Liste keine Zertifikate in der Sperr Liste enthalten sind. Die Sperr Liste wird mithilfe der [**iwmdrmsecurity:: getrevocationdata**](iwmdrmsecurity-getrevocationdata.md) -Methode extrahiert.

Verwenden Sie dann die [**iwmdrmsecurity:: checkcertforsperrungsmethode**](iwmdrmsecurity-checkcertforrevocation.md) , um zu überprüfen, ob das Zertifikat nicht widerrufen wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**DRM-Import**](drm-import.md)
</dt> </dl>

 

 




