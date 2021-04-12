---
title: Ivmguestos SetParameter-Methode (vpccominterfaces. h)
description: Legt einen benannten Parameter innerhalb des Gast Betriebssystems fest.
ms.assetid: ed6ade61-19dc-44ac-9e86-29fffe80e874
keywords:
- SetParameter-Methode Virtual PC
- SetParameter-Methode Virtual PC, ivmguestos-Schnittstelle
- Ivmguestos Interface Virtual PC, SetParameter-Methode
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
ms.openlocfilehash: 80dd2290578ef55d56e4c194e27102a1075d7a10
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517897"
---
# <a name="ivmguestossetparameter-method"></a>Ivmguestos:: SetParameter-Methode

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Legt einen benannten Parameter innerhalb des Gast Betriebssystems fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetParameter(
  [in] BSTR inParameterName,
  [in] BSTR inParameterValue
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*inparametername* \[ in\]
</dt> <dd>

Der Name des Parameters. Der Wert muss zwischen 1 und 255 Zeichen lang sein und darf keinen umgekehrten Schrägstrich ( \) Zeichen) enthalten.

</dd> <dt>

*inparametervalue* \[ in\]
</dt> <dd>

Der Parameterwert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode/-wert                                                                                                                                                                    | BESCHREIBUNG                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                          | Der Vorgang wurde durchgeführt.<br/>                        |
| <dl> <dt>**E \_ InvalidArg**</dt> <dt>0x80000003</dt> </dl>                         | Ein Parameter ist ungültig oder wurde nicht angegeben.<br/>           |
| <dl> <dt>**VM \_ E \_ \_**</dt> Zeitüberschreitung <dt>0xa0040202</dt> </dl>                     | Der Vorgang wurde nicht rechtzeitig beendet.<br/>   |
| <dl> <dt>**VM \_ E \_ - \_ VM \_ führt**</dt> <dt>0xa0040206</dt> nicht aus </dl>               | Der virtuelle Computer (VM) wird nicht ausgeführt.<br/>             |
| <dl> <dt>**VM \_ E- \_ VM \_ angeh**</dt> alten <dt>0xa00400507</dt> </dl>                    | Der virtuelle Computer wurde angehalten.<br/>                                    |
| <dl> <dt>**VM \_ E \_ ADDITIONS \_ - \_ Funktion \_ nicht**</dt> " <dt>uxa0040505</dt> " </dl> | Integrations Komponenten sind auf diesem virtuellen Computer nicht installiert.<br/> |
| <dl> <dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt> </dl>                    | Ein unerwarteter Fehler ist aufgetreten.<br/>                    |



 

## <a name="remarks"></a>Bemerkungen

Der virtuelle Computer muss ausgeführt werden, und Integrations Komponenten müssen installiert werden, wenn diese Methode aufgerufen wird. Diese Methode wird nur für Windows-basierte Gast Betriebssysteme unterstützt.

Wenn Integrations Komponenten installiert sind, wird der folgende Schlüssel der Registrierung des Gast Betriebssystems automatisch hinzugefügt:

**HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ Virtual Machine \\ Guest \\ Parameters**

Wenn das Gast Betriebssystem gestartet wird, werden die folgenden Registrierungszeichen folgen Werte im **Parameter** Schlüssel aufgefüllt:

-   **HostName**
-   **Physicalhostname**
-   **Physicalhostnamefullyqualified**
-   **VirtualMachineName**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Vpccominterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ ivmguestos ist als 99fea0db-4880-499a-b6d8-73dff9bc91be definiert.<br/>                 |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ivmguestos**](ivmguestos.md)
</dt> </dl>

 

