---
title: IVMGuestOS SetParameter-Methode (VPCCOMInterfaces.h)
description: Legt einen benannten Parameter innerhalb des Gastbetriebssystems fest.
ms.assetid: ed6ade61-19dc-44ac-9e86-29fffe80e874
keywords:
- 'SetParameter-Methode : Virtueller PC'
- SetParameter-Methode Virtual PC, IVMGuestOS-Schnittstelle
- IVMGuestOS-Schnittstelle Virtueller PC, SetParameter-Methode
topic_type:
- apiref
api_name:
- IVMGuestOS.SetParameter
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69a8a22257aea0f30d2620d610a2ef3745c9c2a640f034bd1c30d1f582a6c9a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119512300"
---
# <a name="ivmguestossetparameter-method"></a>IVMGuestOS::SetParameter-Methode

\[Windows Der virtuelle PC ist ab diesem Zeitraum nicht mehr Windows 8. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Legt einen benannten Parameter innerhalb des Gastbetriebssystems fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetParameter(
  [in] BSTR inParameterName,
  [in] BSTR inParameterValue
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*inParameterName* \[ In\]
</dt> <dd>

Der Name des Parameters. Er muss zwischen 1 und 255 Zeichen lang sein und darf keinen schrägen Schrägstrich \\ () enthalten.

</dd> <dt>

*inParameterValue* \[ In\]
</dt> <dd>

Der Parameterwert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode/-wert                                                                                                                                                                    | Beschreibung                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                          | Der Vorgang wurde durchgeführt.<br/>                        |
| <dl> <dt>**E \_ INVALIDARG-0x80000003**</dt> <dt></dt> </dl>                         | Ein Parameter ist ungültig oder nicht angegeben.<br/>           |
| <dl> <dt>**VM \_ E \_ TIMED \_ OUT**</dt> <dt>0xA0040202</dt> </dl>                     | Der Vorgang wurde nicht rechtzeitig abgeschlossen.<br/>   |
| <dl> <dt>**VM \_ E \_ VM \_ NOT \_ RUNNING**</dt> <dt>0xA0040206</dt> </dl>               | Der virtuelle Computer (VM) wird nicht ausgeführt.<br/>             |
| <dl> <dt>**VM \_ E \_ VM \_ PAUSED**</dt> <dt>0xA00400507</dt> </dl>                    | Der virtuelle Computer wurde angehalten.<br/>                                    |
| <dl> <dt>**VM \_ E \_ ADDITIONS \_ FEATURE NOT \_ \_ AVAIL**</dt> <dt>0XA0040505</dt> </dl> | Integrationskomponenten sind auf diesem virtuellen Computer nicht installiert.<br/> |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>                    | Ein unerwarteter Fehler ist aufgetreten.<br/>                    |



 

## <a name="remarks"></a>Hinweise

Die VM muss ausgeführt werden, und Integrationskomponenten müssen installiert werden, wenn diese Methode aufgerufen wird. Diese Methode wird nur für Windows Gastbetriebssysteme unterstützt.

Wenn Integrationskomponenten installiert sind, wird der folgende Schlüssel automatisch zur Registrierung des Gastbetriebssystems hinzugefügt:

**HKEY \_ LOCAL \_ MACHINE \\ SOFTWARE \\ Microsoft \\ Virtual Machine \\ Guest \\ Parameters**

Wenn das Gastbetriebssystem gestartet wird, werden die folgenden Registrierungszeichenfolgenwerte im **Parameterschlüssel aufgefüllt:**

-   **HostName**
-   **PhysicalHostName**
-   **PhysicalHostNameFullyQualified**
-   **VirtualMachineName**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMGuestOS ist als 99fea0db-4880-499a-b6d8-73dff9bc91be definiert.<br/>                 |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IVMGuestOS**](ivmguestos.md)
</dt> </dl>

 

