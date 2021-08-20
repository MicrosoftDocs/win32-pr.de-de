---
title: IMsRdpClientNonScriptable5 GetRemoteMonitorsBoundingBox-Eigenschaft
description: Gibt das umgrenzende Rechteck des Remotemonitors an.
ms.assetid: 4A8794F7-1DB4-4415-8538-6B2A365B22D3
ms.tgt_platform: multiple
keywords:
- GetRemoteMonitorsBoundingBox-Eigenschaft Remotedesktopdienste
- GetRemoteMonitorsBoundingBox-Eigenschaft Remotedesktopdienste , IMsRdpClientNonScriptable5-Schnittstelle
- IMsRdpClientNonScriptable5-Schnittstelle Remotedesktopdienste , GetRemoteMonitorsBoundingBox-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable5.GetRemoteMonitorsBoundingBox
- IMsRdpClientNonScriptable5.get_GetRemoteMonitorsBoundingBox
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a47b308bf95389dcf043e87565be365ec69ecc34500ac187ee11a679349f18ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118129888"
---
# <a name="imsrdpclientnonscriptable5getremotemonitorsboundingbox-property"></a>IMsRdpClientNonScriptable5::GetRemoteMonitorsBoundingBox-Eigenschaft

Gibt das umgrenzende Rechteck des Remotemonitors an.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_GetRemoteMonitorsBoundingBox(
  [out] LONG *pLeft,
  [out] LONG *pTop,
  [out] LONG *pRight,
  [out] LONG *pBottom
);
```



## <a name="property-value"></a>Eigenschaftswert

Empfängt den linken Rand des Rechtecks.

Empfängt den oberen Rand des Rechtecks.

Empfängt den rechten Rand des Rechtecks.

Empfängt den unteren Rand des Rechtecks.

## <a name="remarks"></a>Hinweise

Alle Koordinaten befinden sich in virtuellen Bildschirmkoordinaten, die relativ zur oberen linken Ecke des primären Monitors sind. Wenn dies nicht der primäre Monitor ist, können einige oder alle diese Werte negativ sein.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7<br/>                                                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2<br/>                                                             |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>        |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>        |
| IID<br/>                      | \_IID-IMsRdpClientNonScriptable5 ist als 4f6996d5-d7b1-412c-b0ff-063718566907 definiert.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)
</dt> </dl>

 

 





