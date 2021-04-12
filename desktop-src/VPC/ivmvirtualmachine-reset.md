---
title: Ivmvirtualmachine Reset-Methode (vpccominterfaces. h)
description: Setzt den virtuellen Computer zurück.
ms.assetid: 44daf6be-66ce-4291-a535-c30369eed60f
keywords:
- Methode für virtuellen PC zurücksetzen
- Methode "Virtual PC zurücksetzen", ivmvirtualmachine-Schnittstelle
- Ivmvirtualmachine Interface Virtual PC, Methode zurücksetzen
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Reset
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45314eef6d837ac00647d477f3652b63221d977c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478345"
---
# <a name="ivmvirtualmachinereset-method"></a>Ivmvirtualmachine:: Reset-Methode

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Setzt den virtuellen Computer (VM) zurück.

## <a name="syntax"></a>Syntax


```C++
HRESULT Reset(
  [out, retval] IVMTask **resetTask
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*resettask* \[ Out, retval\]
</dt> <dd>

Ein [**ivmtask**](ivmtask.md) -Objekt, das verwendet wird, um den Abschluss Status der zurückgesetzten Sequenz der VM zu verfolgen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode/-wert                                                                                                                                                                          | BESCHREIBUNG                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                | Der Vorgang wurde durchgeführt.<br/>                                     |
| <dl> <dt>**E \_ Zeiger**</dt> <dt>0x80004003</dt> </dl>                                  | Der-Parameter ist **null**.<br/>                                        |
| <dl> <dt>**HRESULT \_ Von \_ Win32 (Fehler \_ Zugriff \_ verweigert)**</dt> <dt>0x80070005</dt> </dl> | Der Aufrufer muss über Execute Access-Berechtigungen verfügen, um diesen virtuellen Computer zurückzusetzen<br/> |
| <dl> <dt>**VM \_ E \_ - \_ VM \_ führt**</dt> <dt>0xa0040206</dt> nicht aus </dl>                     | Der virtuelle Computer wird nicht ausgeführt.<br/>                                            |
| <dl> <dt>**VM \_ E \_ VM \_ unbekannt**</dt> <dt>0xa0040207</dt> </dl>                          | Die Konfiguration ist unbekannt.<br/>                                     |
| <dl> <dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt> </dl>                          | Ein unerwarteter Fehler ist aufgetreten.<br/>                                 |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Vpccominterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ ivmvirtualmachine ist als f7092aa1-33ed-4f78-a59f-c00adfc2edd7 definiert.<br/>          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ivmvirtualmachine**](ivmvirtualmachine.md)
</dt> </dl>

 

