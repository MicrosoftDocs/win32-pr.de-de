---
title: Ivmvirtualpc findvirtualnetwork-Methode (vpccominterfaces. h)
description: Ruft ein virtuelles Netzwerk Objekt ab, das mit dem angeforderten Namen übereinstimmt.
ms.assetid: 84526fa4-fe88-4466-866d-c432ed3125aa
keywords:
- Findvirtualnetwork-Methode Virtual PC
- Findvirtualnetwork-Methode Virtual PC, ivmvirtualpc-Schnittstelle
- Ivmvirtualpc Interface Virtual PC, findvirtualnetwork-Methode
topic_type:
- apiref
api_name:
- IVMVirtualPC.FindVirtualNetwork
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c59306d2e2022c1323ab52f1a47bd386347f504e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518470"
---
# <a name="ivmvirtualpcfindvirtualnetwork-method"></a>Ivmvirtualpc:: findvirtualnetwork-Methode

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Ruft ein virtuelles Netzwerk Objekt ab, das mit dem angeforderten Namen übereinstimmt.

## <a name="syntax"></a>Syntax


```C++
HRESULT FindVirtualNetwork(
  [in]          BSTR              virtualNetworkName,
  [out, retval] IVMVirtualNetwork **virtualNetwork
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*virtualnetworkname* \[ in\]
</dt> <dd>

Der Name des zu suchenden virtuellen Netzwerks.

</dd> <dt>

*VirtualNetwork* \[ Out, retval\]
</dt> <dd>

Ein Zeiger auf ein neues [**ivmvirtualnetwork**](ivmvirtualnetwork.md) -Objekt, das dieses virtuelle Netzwerk darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode/-wert                                                                                                                                                                            | BESCHREIBUNG                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                  | Der Vorgang wurde durchgeführt.<br/>                                                        |
| <dl> <dt>**S \_ Falsch**</dt> <dt>1</dt> </dl>                                               | Das angegebene virtuelle Netzwerk konnte nicht gefunden werden.<br/>                                    |
| <dl> <dt>**E \_ Zeiger**</dt> <dt>0x80004003</dt> </dl>                                    | Der *VirtualNetwork* -Parameter ist **null** , oder das virtuelle Netzwerk kann nicht gefunden werden.<br/>   |
| <dl> <dt>**E \_ InvalidArg**</dt> <dt>0x80000003</dt> </dl>                                 | Der Parameter " *virtualnetworkname* " ist ungültig oder eine leere Zeichenfolge.<br/>               |
| <dl> <dt>**HRESULT \_ Von \_ Win32 (Fehler \_ Datei \_ nicht \_ gefunden)**</dt> <dt>0x80070002</dt> </dl> | Die virtuelle Netzwerkdatei konnte nicht gefunden werden.<br/>                                         |
| <dl> <dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt> </dl>                            | Ein unerwarteter Fehler ist aufgetreten.<br/>                                                    |
| <dl> <dt>**VM \_ E \_ \_ Hardwarevirtualisierung \_ deaktiviert**</dt> <dt>0xa0040951</dt> </dl>     | Der Prozessor bietet keine Unterstützung für hav-Erweiterungen (Hardware Beschleunigung Virtualization).<br/> |



 

## <a name="remarks"></a>Bemerkungen

Bei Namen von virtuellen Netzwerken wird die Groß-/Kleinschreibung nicht beachtet, z. b. "mynetwork" und "mynetwork" beziehen sich auf dasselbe virtuelle Netzwerk.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Vpccominterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ ivmvirtualpc ist als 236ba0d9-a24a-4292-A132-27c1421dfd01 definiert.<br/>               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ivmvirtualpc**](ivmvirtualpc.md)
</dt> </dl>

 

