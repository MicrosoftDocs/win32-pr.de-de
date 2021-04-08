---
title: IMsRdpClientNonScriptable5 getremotemonitorsboundingbox-Eigenschaft
description: Gibt das Begrenzungs Rechteck des Remote Monitors an.
ms.assetid: 4A8794F7-1DB4-4415-8538-6B2A365B22D3
ms.tgt_platform: multiple
keywords:
- Getremotemonitorsboundingbox-Eigenschaft Remotedesktopdienste
- Getremotemonitorsboundingbox-Eigenschaft Remotedesktopdienste, IMsRdpClientNonScriptable5-Schnittstelle
- IMsRdpClientNonScriptable5 Interface Remotedesktopdienste, getremotemonitorsboundingbox-Eigenschaft
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
ms.openlocfilehash: 97f67192b78c734359fc6113969eb5eb410e1bf3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956757"
---
# <a name="imsrdpclientnonscriptable5getremotemonitorsboundingbox-property"></a>IMsRdpClientNonScriptable5:: getremotemonitorsboundingbox-Eigenschaft

Gibt das Begrenzungs Rechteck des Remote Monitors an.

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

## <a name="remarks"></a>Bemerkungen

Alle Koordinaten befinden sich in den virtuellen Bildschirm Koordinaten, die relativ zur oberen linken Ecke des primären Monitors sind. Wenn dies nicht der primäre Monitor ist, können einige oder alle dieser Werte negativ sein.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7<br/>                                                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2<br/>                                                             |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>        |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>        |
| IID<br/>                      | IID \_ IMsRdpClientNonScriptable5 ist als 4f 6996d5-d7b1-412c-b0ff-063718566907 definiert.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)
</dt> </dl>

 

 





