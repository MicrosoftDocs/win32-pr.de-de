---
title: Ivmhostinfo processorfeaturesstring-Eigenschaft (vpccominterfaces. h)
description: Ruft die Listen Features ab, die vom Host Prozessor unterstützt werden.
ms.assetid: 036c6376-0e9b-46fa-90f4-a40c71c5cf23
keywords:
- Processorfeaturesstring-Eigenschaft virtueller PC
- Processorfeaturesstring-Eigenschaft Virtual PC, ivmhostinfo-Schnittstelle
- Ivmhostinfo Interface Virtual PC, processorfeaturesstring (Eigenschaft)
topic_type:
- apiref
api_name:
- IVMHostInfo.ProcessorFeaturesString
- IVMHostInfo.get_ProcessorFeaturesString
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 118aaa2eabe7ddb2fd608892775a17eac6a77d16
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106337487"
---
# <a name="ivmhostinfoprocessorfeaturesstring-property"></a>Ivmhostinfo::P rocess orfeaturesstring-Eigenschaft

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Ruft die Listen Features ab, die vom Host Prozessor unterstützt werden.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_ProcessorFeaturesString(
  [out, retval] BSTR *featuresString
);
```



## <a name="property-value"></a>Eigenschaftswert

Eine durch Trennzeichen getrennte Liste von Features. Ein Beispiel wäre "MMX, SSE, SSE2, x86-64".



| Wert                                                                                 | Bedeutung                                                             |
|---------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <dt>"AMD-V"</dt> </dl>    | Unterstützt die AMD-Virtualisierungserweiterungen.<br/>              |
| <dl> <dt>"Intel VT"</dt> </dl> | Unterstützt die Intel Virtualization Technology Extensions.<br/> |
| <dl> <dt>"Havd"</dt> </dl>     | Die Hardware gestützte Virtualisierung ist deaktiviert.<br/>            |
| <dl> <dt>Hätten</dt> </dl>     | Die Hardware gestützte Virtualisierung ist aktiviert.<br/>             |
| <dl> <dt>MMX</dt> </dl>      | Unterstützt die MMX-Erweiterungen.<br/>                             |
| <dl> <dt>Preußen</dt> </dl>      | Unterstützt die Streaming SIMD Extensions.<br/>                  |
| <dl> <dt>SSE2</dt> </dl>     | Unterstützt die Streaming SIMD Extensions 2.<br/>                |
| <dl> <dt>SSE3</dt> </dl>     | Unterstützt die Streaming SIMD Extensions 3.<br/>                |
| <dl> <dt>"Txte"</dt> </dl>     | Unterstützt die Erweiterungen der vertrauenswürdigen Ausführungs Technologie.<br/>    |
| <dl> <dt>"x86-64"</dt> </dl>   | Unterstützt x86-64-Erweiterungen.<br/>                              |



 

## <a name="error-codes"></a>Fehlercodes



| Name/Wert                                                                                                                                                    | Bedeutung                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | Der Vorgang wurde durchgeführt.<br/>     |
| <dl> <dt>E \_ Zeiger</dt> <dt>0x80004003</dt> </dl>         | Der-Parameter ist **null**.<br/>        |
| <dl> <dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt> </dl> | Ein unerwarteter Fehler ist aufgetreten.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Vpccominterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ ivmhostinfo ist als 5b5cf343-05ad-453b-be99-adf4e27b2ebc definiert.<br/>                |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ivmhostinfo**](ivmhostinfo.md)
</dt> </dl>

 

