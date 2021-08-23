---
title: IVMHostInfo ProcessorFeaturesString-Eigenschaft (VPCCOMInterfaces.h)
description: Ruft die vom Hostprozessor unterstützten Listenfeatures ab.
ms.assetid: 036c6376-0e9b-46fa-90f4-a40c71c5cf23
keywords:
- ProcessorFeaturesString-Eigenschaft Virtueller PC
- ProcessorFeaturesString-Eigenschaft Virtueller PC, IVMHostInfo-Schnittstelle
- IVMHostInfo-Schnittstelle Virtueller PC , ProcessorFeaturesString-Eigenschaft
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
ms.openlocfilehash: 1040702df250c906bb32af5068a340c37a9ba3faabee3af17d8397bfdc8059e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998890"
---
# <a name="ivmhostinfoprocessorfeaturesstring-property"></a>IVMHostInfo::P rocessorFeaturesString-Eigenschaft

\[Windows Der virtuelle PC ist ab Windows 8 nicht mehr für die Verwendung verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Ruft die vom Hostprozessor unterstützten Listenfeatures ab.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_ProcessorFeaturesString(
  [out, retval] BSTR *featuresString
);
```



## <a name="property-value"></a>Eigenschaftswert

Eine durch Trennzeichen getrennte Liste von Features. Ein Beispiel wäre "MMX,SSE,SSE2,x86-64".



| Wert                                                                                 | Bedeutung                                                             |
|---------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <dt>"AMD-V"</dt> </dl>    | Unterstützt die AMD-Virtualisierungserweiterungen.<br/>              |
| <dl> <dt>"Intel VT"</dt> </dl> | Unterstützt die Intel Virtualization Technology-Erweiterungen.<br/> |
| <dl> <dt>"HAVD"</dt> </dl>     | Die hardwareunterstützte Virtualisierung ist deaktiviert.<br/>            |
| <dl> <dt>"HAVE"</dt> </dl>     | Die hardwareunterstützte Virtualisierung ist aktiviert.<br/>             |
| <dl> <dt>"MMX"</dt> </dl>      | Unterstützt die MMX-Erweiterungen.<br/>                             |
| <dl> <dt>"SSE"</dt> </dl>      | Unterstützt die Streaming SIMD Extensions.<br/>                  |
| <dl> <dt>"SSE2"</dt> </dl>     | Unterstützt die Streaming SIMD Extensions 2.<br/>                |
| <dl> <dt>"SSE3"</dt> </dl>     | Unterstützt die Streaming SIMD Extensions 3.<br/>                |
| <dl> <dt>"TXTE"</dt> </dl>     | Unterstützt die Erweiterungen der vertrauenswürdigen Ausführungstechnologie.<br/>    |
| <dl> <dt>"x86-64"</dt> </dl>   | Unterstützt x86-64-Erweiterungen.<br/>                              |



 

## <a name="error-codes"></a>Fehlercodes



| Name/Wert                                                                                                                                                    | Bedeutung                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | Der Vorgang wurde durchgeführt.<br/>     |
| <dl> <dt>E \_ POINTER</dt> <dt>0x80004003</dt> </dl>         | Der Parameter ist **NULL.**<br/>        |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl> | Ein unerwarteter Fehler ist aufgetreten.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Product (Produkt)<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMHostInfo ist als 5b5cf343-05ad-453b-be99-adf4e27b2ebc definiert.<br/>                |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IVMHostInfo**](ivmhostinfo.md)
</dt> </dl>

 

