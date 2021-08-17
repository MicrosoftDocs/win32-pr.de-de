---
title: IMsRdpClientNonScriptable3 DriveCollection-Eigenschaft
description: Ruft die Auflistung der Laufwerkobjekte ab, die umgeleitet werden sollen.
ms.assetid: 5aaac605-584b-442e-9d67-1cb8213a70b3
ms.tgt_platform: multiple
keywords:
- DriveCollection-Eigenschaft Remotedesktopdienste
- DriveCollection-Eigenschaft Remotedesktopdienste , IMsRdpClientNonScriptable3-Schnittstelle
- IMsRdpClientNonScriptable3-Schnittstelle Remotedesktopdienste , DriveCollection-Eigenschaft
- DriveCollection-Eigenschaft Remotedesktopdienste , IMsRdpClientNonScriptable4-Schnittstelle
- IMsRdpClientNonScriptable4-Schnittstelle Remotedesktopdienste , DriveCollection-Eigenschaft
- DriveCollection-Eigenschaft Remotedesktopdienste , IMsRdpClientNonScriptable5-Schnittstelle
- IMsRdpClientNonScriptable5-Schnittstelle Remotedesktopdienste , DriveCollection-Eigenschaft
- DriveCollection-Eigenschaft Remotedesktopdienste , MsRdpClient5-Objekt
- MsRdpClient5-Objekt Remotedesktopdienste , DriveCollection-Eigenschaft
- DriveCollection-Eigenschaft Remotedesktopdienste , MsRdpClient6-Objekt
- MsRdpClient6-Objekt Remotedesktopdienste , DriveCollection-Eigenschaft
- DriveCollection-Eigenschaft Remotedesktopdienste , MsRdpClient7-Objekt
- MsRdpClient7-Objekt Remotedesktopdienste , DriveCollection-Eigenschaft
- DriveCollection-Eigenschaft Remotedesktopdienste , MsRdpClient8-Objekt
- MsRdpClient8-Objekt Remotedesktopdienste , DriveCollection-Eigenschaft
- DriveCollection-Eigenschaft Remotedesktopdienste , MsRdpClient9-Objekt
- MsRdpClient9-Objekt Remotedesktopdienste , DriveCollection-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3.DriveCollection
- IMsRdpClientNonScriptable3.get_DriveCollection
- IMsRdpClientNonScriptable4.DriveCollection
- IMsRdpClientNonScriptable4.get_DriveCollection
- IMsRdpClientNonScriptable5.DriveCollection
- IMsRdpClientNonScriptable5.get_DriveCollection
- MsRdpClient5.DriveCollection
- MsRdpClient6.DriveCollection
- MsRdpClient7.DriveCollection
- MsRdpClient8.DriveCollection
- MsRdpClient9.DriveCollection
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95cc25d53014936e3adab4f12d5c92cfcbb7b35c7b663c4a2c1f7f77fb467fb4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119001140"
---
# <a name="imsrdpclientnonscriptable3drivecollection-property"></a>IMsRdpClientNonScriptable3::D riveCollection-Eigenschaft

Ruft die Auflistung der Laufwerkobjekte ab, die umgeleitet werden sollen.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_DriveCollection(
  [out] IMsRdpDriveCollection **ppDriveCollection
);
```



## <a name="property-value"></a>Eigenschaftswert

Ruft die Auflistung von Laufwerkobjekten vom Typ [**IMSRdpDrive**](imsrdpdrive.md)ab.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                                |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>        |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>        |
| IID<br/>                      | IID \_ IMsRdpClientNonScriptable3 ist als b3378d90-0728-45c7-8ed7-b6159fb92219 definiert.<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IMsRdpClientNonScriptable4**](imsrdpclientnonscriptable4.md)
</dt> <dt>

[**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)
</dt> <dt>

[**IMsRdpClientNonScriptable3**](imsrdpclientnonscriptable3.md)
</dt> </dl>

 

 





