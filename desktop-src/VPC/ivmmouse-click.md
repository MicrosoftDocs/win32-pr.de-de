---
title: Ivmmouse-Click-Methode (vpccominterfaces. h)
description: Simuliert das Klicken auf die Maustaste.
ms.assetid: f16e36d6-34ca-4d65-95e4-1a6660d0abd0
keywords:
- Klicken Sie auf method Virtual PC.
- Klicken Sie auf Methode Virtual PC, ivmmouse Interface.
- Ivmmouse Interface Virtual PC, klicken Sie auf Methode.
topic_type:
- apiref
api_name:
- IVMMouse.Click
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad3ea1b861db0a92ad92e689770182d225778aee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478999"
---
# <a name="ivmmouseclick-method"></a>Ivmmouse:: Click-Methode

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Simuliert das Klicken auf die Maustaste.

## <a name="syntax"></a>Syntax


```C++
HRESULT Click(
  [in] VMMouseButton buttonIndex
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ButtonIndex* \[ in\]
</dt> <dd>

Der Index der Schaltfläche, auf die geklickt wird. Eine Liste der Werte finden Sie unter [**vmmousetbutton**](vmmousebutton.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode/-wert                                                                                                                                                        | BESCHREIBUNG                                                                                                                                       |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                              | Der Vorgang wurde durchgeführt.<br/>                                                                                                          |
| <dl> <dt>**E \_ InvalidArg**</dt> <dt>0x80000003</dt> </dl>             | Der-Parameter ist **null**.<br/>                                                                                                             |
| <dl> <dt>**VM \_ E \_ - \_ VM \_ führt**</dt> <dt>0xa0040206</dt> nicht aus </dl>   | Der virtuelle Computer, an den dieses Mausgerät angefügt ist, wird zurzeit nicht ausgeführt.<br/>                                                   |
| <dl> <dt>**VM \_ E \_ Maus \_ nicht \_ aktiv**</dt> <dt>0xa0040800</dt> </dl> | Der Vorgang konnte nicht abgeschlossen werden, da das Mausgerät nicht eingeschaltet ist oder derzeit nicht auf dem virtuellen Computer aktiv ist.<br/> |
| <dl> <dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt> </dl>        | Ein unerwarteter Fehler ist aufgetreten.<br/>                                                                                                      |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Vpccominterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ ivmmouse ist als ac903f6d-6346-4f29-8875-5d511a13895e definiert.<br/>                   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ivmmouse**](ivmmouse.md)
</dt> </dl>

 

