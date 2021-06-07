---
title: IVMGuestOS GetParameter-Methode (VPCCOMInterfaces.h)
description: Ruft einen benannten Parameter im Gastbetriebssystem ab.
ms.assetid: d4d5acbd-fa19-4eb2-af75-2c94e5f6f7f0
keywords:
- GetParameter-Methode Virtueller PC
- GetParameter-Methode Virtueller PC, IVMGuestOS-Schnittstelle
- IVMGuestOS-Schnittstelle Virtueller PC, GetParameter-Methode
topic_type:
- apiref
api_name:
- IVMGuestOS.GetParameter
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d12bddec3fac5dc918f06d926fe5e5656b70d84d
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387646"
---
# <a name="ivmguestosgetparameter-method"></a>IVMGuestOS::GetParameter-Methode

\[Windows Virtual PC ist ab Windows 8 nicht mehr für die Verwendung verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Ruft einen benannten Parameter im Gastbetriebssystem ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetParameter(
  [in]          BSTR inParameterName,
  [out, retval] BSTR *outParameterValue
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*inParameterName* \[ In\]
</dt> <dd>

Der Name des Parameters. Er muss zwischen 1 und 255 Zeichen lang sein und darf keinen umgekehrten Schrägstrich \\ () enthalten.

</dd> <dt>

*outParameterValue* \[ out, retval\]
</dt> <dd>

Der Parameterwert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode/-wert                                                                                                                                                                    | BESCHREIBUNG                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                          | Der Vorgang wurde durchgeführt.<br/>                                     |
| <dl> <dt>**E \_ INVALIDARG-0x80000003**</dt> <dt></dt> </dl>                         | Ein Parameter ist ungültig oder nicht angegeben.<br/>                        |
| <dl> <dt>**E \_ POINTER**</dt> <dt>0x80004003</dt> </dl>                            | Der Parameter ist **NULL.**<br/>                                        |
| <dl> <dt>**VM \_ E \_ TIMED \_ OUT**</dt> <dt>0xA0040202</dt> </dl>                     | Der Vorgang wurde nicht rechtzeitig abgeschlossen.<br/>                |
| <dl> <dt>**VM \_ E \_ VM WIRD NICHT \_ \_ AUSGEFÜHRT**</dt> <dt>0xA0040206</dt> </dl>               | Der virtuelle Computer wird nicht ausgeführt.<br/>                               |
| <dl> <dt>**VM \_ E \_ VM \_ PAUSED**</dt> <dt>0xA00400507</dt> </dl>                    | Der virtuelle Computer wird angehalten.<br/>                                    |
| <dl> <dt>**VM \_ E \_ ADDITIONS \_ FEATURE NOT \_ \_ AVAIL**</dt> <dt>0XA0040505</dt> </dl> | Integrationskomponenten werden auf diesem virtuellen Computer nicht installiert.<br/> |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>                    | Ein unerwarteter Fehler ist aufgetreten.<br/>                                 |



 

## <a name="remarks"></a>Hinweise

Der virtuelle Computer muss ausgeführt werden, und Integrationskomponenten müssen installiert werden, wenn diese Methode aufgerufen wird. Diese Methode wird nur für Windows-basierte Gastbetriebssysteme unterstützt.

Bei installierten Integrationskomponenten wird der Registrierung des Gastbetriebssystems automatisch der folgende Schlüssel hinzugefügt:

**HKEY \_ LOCAL \_ MACHINE \\ SOFTWARE \\ Microsoft \\ Virtual Machine \\ Guest \\ Parameters**

Wenn das Gastbetriebssystem gestartet wird, werden die folgenden Werte der Registrierungszeichenfolge im **Parameterschlüssel** aufgefüllt:

-   **HostName**
-   **PhysicalHostName**
-   **PhysicalHostNameFullyQualified**
-   **VirtualMachineName**

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows \[ 7-Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMGuestOS ist als 99fea0db-4880-499a-b6d8-73dff9bc91be definiert.<br/>                 |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IVMGuestOS**](ivmguestos.md)
</dt> </dl>

 

