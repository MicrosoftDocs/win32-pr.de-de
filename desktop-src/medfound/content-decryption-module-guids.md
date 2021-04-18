---
description: Die folgenden GUIDs unterstützen CDM-Implementierungen (Content entschlüsseln Module).
title: CDM-GUIDs (Content Decryption Module)
ms.topic: reference
ms.date: 01/21/2018
ms.openlocfilehash: e06601fd23d3244d0965d2cfd7cd70a6f73a481f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364690"
---
# <a name="content-decryption-module-cdm-guids"></a>CDM-GUIDs (Content Decryption Module)

Die folgenden GUIDs unterstützen CDM-Implementierungen (Content entschlüsseln Module).

**MF_CONTENTDECRYPTIONMODULE_SERVICE**

Dienst-GUID, die zum Abrufen von Schnittstellen aus einer [imfcontentdecryptionmodule](/windows/win32/api/mfcontentdecryptionmodule/nn-mfcontentdecryptionmodule-imfcontentdecryptionmodule) -Implementierung verwendet wird, z. b. die WinRT-Schnittstelle [imediaschutzpmpserver](/uwp/api/windows.media.protection.mediaprotectionpmpserver) Eine Implementierung von **IMF contentdecryptionmodule** sollte [IMF](/windows/win32/api/mfidl/nn-mfidl-imfgetservice) implementieren und diese Dienst-GUID unterstützen.


## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>MF contentdecryptionmodule. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch



- [Media Foundation Konstanten](media-foundation-constants.md)
- [IMF contentdecryptionmodule] (/windows/win32/api/mfcontentdecryptionmodule/nn-mfcontentdecryptionmodule-imfcontentdecryptionmodule
- [Imediaschutzpmpserver](/uwp/api/windows.media.protection.mediaprotectionpmpserver)
- [IMF-Dienst](/windows/win32/api/mfidl/nn-mfidl-imfgetservice)


 

 




