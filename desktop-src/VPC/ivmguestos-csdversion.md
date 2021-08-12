---
title: IVMGuestOS CSDVersion-Eigenschaft (VPCCOMInterfaces.h)
description: Die CSDVersion des Gastbetriebssystems, das auf dem virtuellen Computer ausgeführt wird.
ms.assetid: 6f1d8dd6-6feb-4bdf-a553-631d55c18076
keywords:
- CSDVersion-Eigenschaft Virtueller PC
- CSDVersion-Eigenschaft Virtueller PC, IVMGuestOS-Schnittstelle
- IVMGuestOS-Schnittstelle Virtueller PC, CSDVersion-Eigenschaft
topic_type:
- apiref
api_name:
- IVMGuestOS.CSDVersion
- IVMGuestOS.get_CSDVersion
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab4d4d1594311aff0a95795dc2501a7eff9767a233033f76bc1d5c0c9e6c7933
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118594339"
---
# <a name="ivmguestoscsdversion-property"></a>IVMGuestOS::CSDVersion-Eigenschaft

\[Windows Der virtuelle PC ist ab diesem Zeitraum nicht mehr Windows 8. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Ruft die CSDVersion des Gastbetriebssystems ab, das auf dem virtuellen Computer ausgeführt wird.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_CSDVersion(
  [out, retval] BSTR *csdVersion
);
```



## <a name="property-value"></a>Eigenschaftswert

Eine auf NULL beendete Zeichenfolge, z. B. "Service Pack 3", die das neueste auf dem System installierte Service Pack angibt. Wenn kein Service Pack installiert wurde, ist die Zeichenfolge leer.

## <a name="error-codes"></a>Fehlercodes



| Name/Wert                                                                                                                                                                       | Bedeutung                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                          | Der Vorgang wurde durchgeführt.<br/>                        |
| <dl> <dt>E \_ ZEIGER 0X80004003</dt> <dt></dt> </dl>                            | Der Parameter ist **NULL.**<br/>                           |
| <dl> <dt>VM \_ E \_ VM \_ NOT \_ RUNNING</dt> <dt>0xA0040206</dt> </dl>               | Der virtuelle Computer wird nicht ausgeführt.<br/>                               |
| <dl> <dt>VM \_ E \_ ADDITIONS \_ FEATURE NOT \_ \_ AVAIL</dt> <dt>0XA0040505</dt> </dl> | Integrationskomponenten sind auf diesem virtuellen Computer nicht installiert.<br/> |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl>                    | Ein unerwarteter Fehler ist aufgetreten.<br/>                    |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMGuestOS ist als 99fea0db-4880-499a-b6d8-73dff9bc91be definiert.<br/>                 |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IVMGuestOS**](ivmguestos.md)
</dt> </dl>

 

