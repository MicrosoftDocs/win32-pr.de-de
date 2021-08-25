---
description: Die folgenden GUIDs unterstützen CDM-Implementierungen (Content Decryption Module).
title: CDM-GUIDs (Content Decryption Module)
ms.topic: reference
ms.date: 01/21/2018
ms.openlocfilehash: ef4016b731b492ed61c6aed859a905446de72c308e03a734aa3cc8f573645668
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119958780"
---
# <a name="content-decryption-module-cdm-guids"></a>CDM-GUIDs (Content Decryption Module)

Die folgenden GUIDs unterstützen CDM-Implementierungen (Content Decryption Module).

**MF_CONTENTDECRYPTIONMODULE_SERVICE**

Dienst-GUID, die verwendet wird, um Schnittstellen aus einer [IMPLEMENTATION VONCONTENTDecryptionModule](/windows/win32/api/mfcontentdecryptionmodule/nn-mfcontentdecryptionmodule-imfcontentdecryptionmodule) abzurufen, z. B. der WinRT [IMediaProtectionPMPServer-Schnittstelle.](/uwp/api/windows.media.protection.mediaprotectionpmpserver) Eine Implementierung von **"CONTENTContentDecryptionModule"** sollte ["CSVGetService"](/windows/win32/api/mfidl/nn-mfidl-imfgetservice) implementieren und diese Dienst-GUID unterstützen.


## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>mfcontentdecryptionmodule.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch



- [Media Foundation Konstanten](media-foundation-constants.md)
- [CONTENTContentDecryptionModule] (/windows/win32/api/mfcontentdecryptionmodule/nn-mfcontentdecryptionmodule-contentdecryptionmodule
- [IMediaProtectionPMPServer](/uwp/api/windows.media.protection.mediaprotectionpmpserver)
- [VERZRGETService](/windows/win32/api/mfidl/nn-mfidl-imfgetservice)


 

 




