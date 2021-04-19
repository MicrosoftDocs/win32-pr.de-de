---
title: Imsrdpclientshell rdpfilecontents (Eigenschaft)
description: Gibt den Inhalt der Remotedesktopprotokoll Datei (RDP) an, die von Remotedesktop Webzugriff (RD-Webzugriff) oder einem anderen Webportal gestartet werden soll, oder ruft ihn ab.
ms.assetid: fcf37221-0fd5-41fd-83da-7fafc1aff944
ms.tgt_platform: multiple
keywords:
- Rdpfilecontents-Eigenschaft Remotedesktopdienste
- Rdpfilecontents-Eigenschaft Remotedesktopdienste, imsrdpclientshell-Schnittstelle
- Imsrdpclientshell-Schnittstelle Remotedesktopdienste, rdpfilecontents-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientShell.RdpFileContents
- IMsRdpClientShell.get_RdpFileContents
- IMsRdpClientShell.put_RdpFileContents
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed2d1c682c06415757f29f2226f48970f4268800
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342226"
---
# <a name="imsrdpclientshellrdpfilecontents-property"></a>Imsrdpclientshell:: rdpfilecontents-Eigenschaft

Gibt den Inhalt der Remotedesktopprotokoll Datei (RDP) an, die von Remotedesktop Webzugriff (RD-Webzugriff) oder einem anderen Webportal gestartet werden soll, oder ruft ihn ab.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_RdpFileContents(
  [in]  BSTR newVal
);

HRESULT get_RdpFileContents(
  [out] BSTR *pszRdpFile
);
```



## <a name="property-value"></a>Eigenschaftswert

Gibt den Inhalt der RDP-Datei an, die über das Webportal gestartet werden soll.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                         |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ imsrdpclientshell ist als d012ae6d-C19A-4bfe-b367-201f8911f134 definiert.<br/>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Imsrdpclientshell**](imsrdpclientshell.md)
</dt> </dl>

 

 





