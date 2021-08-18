---
title: IMsRdpClientNonScriptable5 RemoteMonitorLayoutMatchesLocal-Eigenschaft
description: Gibt an, ob das Remotemonitorlayout mit dem Layout des lokalen Monitors identisch ist.
ms.assetid: 8F3C6650-870C-417C-82FC-E145FC360012
ms.tgt_platform: multiple
keywords:
- RemoteMonitorLayoutMatchesLocal-Eigenschaft Remotedesktopdienste
- RemoteMonitorLayoutMatchesLocal-Eigenschaft Remotedesktopdienste , IMsRdpClientNonScriptable5-Schnittstelle
- IMsRdpClientNonScriptable5-Schnittstelle Remotedesktopdienste , RemoteMonitorLayoutMatchesLocal-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable5.RemoteMonitorLayoutMatchesLocal
- IMsRdpClientNonScriptable5.get_RemoteMonitorLayoutMatchesLocal
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 235879a80e7e2a90207ee9b7852e73a26874c0961d7394fa80f2cf85e7452362
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119138723"
---
# <a name="imsrdpclientnonscriptable5remotemonitorlayoutmatcheslocal-property"></a>IMsRdpClientNonScriptable5::RemoteMonitorLayoutMatchesLocal-Eigenschaft

Gibt an, ob das Remotemonitorlayout mit dem Layout des lokalen Monitors identisch ist. Wenn diese Eigenschaft **VARIANT \_ TRUE** enthält, ist das Remotemonitorlayout mit dem Layout des lokalen Monitors identisch. Wenn diese Eigenschaft **VARIANT \_ FALSE** enthält, weisen die Remote- und lokalen Monitore unterschiedliche Layouts auf.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_RemoteMonitorLayoutMatchesLocal(
  [out, retval] VARIANT_BOOL *pfRemoteMatchesLocal
);
```



## <a name="property-value"></a>Eigenschaftswert

Empfängt den Eigenschaftswert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7<br/>                                                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2<br/>                                                             |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>        |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>        |
| IID<br/>                      | \_IID-IMsRdpClientNonScriptable5 ist als 4f6996d5-d7b1-412c-b0ff-063718566907 definiert.<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)
</dt> </dl>

 

 





