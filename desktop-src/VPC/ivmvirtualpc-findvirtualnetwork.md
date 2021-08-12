---
title: IVMVirtualPC FindVirtualNetwork-Methode (VPCCOMInterfaces.h)
description: Ruft ein virtuelles Netzwerkobjekt ab, das dem angeforderten Namen entspricht.
ms.assetid: 84526fa4-fe88-4466-866d-c432ed3125aa
keywords:
- FindVirtualNetwork-Methode Virtueller PC
- FindVirtualNetwork-Methode Virtueller PC, IVMVirtualPC-Schnittstelle
- IVMVirtualPC-Schnittstelle Virtueller PC , FindVirtualNetwork-Methode
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
ms.openlocfilehash: cc8cfb0b8f9b7ee5be7bfb25d7d4cd7ca7b215bcf1824262c576038e75e6ce0c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118592135"
---
# <a name="ivmvirtualpcfindvirtualnetwork-method"></a>IVMVirtualPC::FindVirtualNetwork-Methode

\[Windows Der virtuelle PC ist ab Windows 8 nicht mehr für die Verwendung verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Ruft ein virtuelles Netzwerkobjekt ab, das dem angeforderten Namen entspricht.

## <a name="syntax"></a>Syntax


```C++
HRESULT FindVirtualNetwork(
  [in]          BSTR              virtualNetworkName,
  [out, retval] IVMVirtualNetwork **virtualNetwork
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*virtualNetworkName* \[ In\]
</dt> <dd>

Der Name des zu suchender virtuellen Netzwerks.

</dd> <dt>

*virtualNetwork* \[ out, retval\]
</dt> <dd>

Ein Zeiger auf ein neues [**IVMVirtualNetwork-Objekt,**](ivmvirtualnetwork.md) das dieses virtuelle Netzwerk darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode/-wert                                                                                                                                                                            | BESCHREIBUNG                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                  | Der Vorgang wurde durchgeführt.<br/>                                                        |
| <dl> <dt>**S \_ FALSE**</dt> <dt>1</dt> </dl>                                               | Das angegebene virtuelle Netzwerk wurde nicht gefunden.<br/>                                    |
| <dl> <dt>**E \_ POINTER**</dt> <dt>0x80004003</dt> </dl>                                    | Der *parameter virtualNetwork* ist **NULL,** oder das virtuelle Netzwerk wurde nicht gefunden.<br/>   |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>                                 | Der *parameter virtualNetworkName* ist ungültig oder eine leere Zeichenfolge.<br/>               |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ FILE NOT \_ \_ FOUND)**</dt> <dt>0x80070002</dt> </dl> | Die Datei des virtuellen Netzwerks wurde nicht gefunden.<br/>                                         |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>                            | Ein unerwarteter Fehler ist aufgetreten.<br/>                                                    |
| <dl> <dt>**VM \_ E \_ \_ HARDWAREVIRTUALISIERUNG \_ DEAKTIVIERT**</dt> <dt>0xA0040951</dt> </dl>     | Der Prozessor unterstützt keine HAV-Erweiterungen (Hardware Accelerated Virtualization).<br/> |



 

## <a name="remarks"></a>Bemerkungen

Bei Namen virtueller Netzwerke wird die Groß-/Kleinschreibung nicht beachtet, z. B. beziehen sich "MyNetwork" und "mynetwork" auf dasselbe virtuelle Netzwerk.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualPC ist als 236ba0d9-a24a-4292-a132-27c1421dfd01 definiert.<br/>               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IVMVirtualPC**](ivmvirtualpc.md)
</dt> </dl>

 

