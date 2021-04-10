---
title: Ivmguestos-Logoff-Methode (vpccominterfaces. h)
description: Protokolliert alle Benutzer vom Gast Betriebssystem.
ms.assetid: 224aa7cb-0892-4e8a-84bd-78dd5cb724df
keywords:
- Abmelde Methode Virtual PC
- Logoff-Methode Virtual PC, ivmguestos-Schnittstelle
- Ivmguestos Interface Virtual PC, Logoff-Methode
topic_type:
- apiref
api_name:
- IVMGuestOS.Logoff
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20c67e917cc9ff93d162bc340185f426fe9eee3d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040967"
---
# <a name="ivmguestoslogoff-method"></a>Ivmguestos:: Logoff-Methode

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Protokolliert alle Benutzer vom Gast Betriebssystem.

## <a name="syntax"></a>Syntax


```C++
HRESULT Logoff(
  [out, retval] IVMTask **outLogoffTask
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*outlogofftask* \[ Out, retval\]
</dt> <dd>

Ein [**ivmtask**](ivmtask.md) -Objekt, das verwendet wird, um den Abschluss Status der Abmelde Sequenz zu verfolgen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode/-wert                                                                                                                                                                          | BESCHREIBUNG                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                | Der Vorgang wurde durchgeführt.<br/>                                                |
| <dl> <dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt> </dl>                          | Ein unerwarteter Fehler ist aufgetreten.<br/>                                            |
| <dl> <dt>**E \_ Zeiger**</dt> <dt>0x80004003</dt> </dl>                                  | Der-Parameter ist **null**.<br/>                                                   |
| <dl> <dt>**HRESULT \_ Von \_ Win32 (Fehler \_ Zugriff \_ verweigert)**</dt> <dt>0x80070005</dt> </dl> | Der Aufrufer muss über Berechtigungen zum Ausführen des Zugriffs auf diese VM verfügen.<br/>                 |
| <dl> <dt>**VM \_ E \_ \_**</dt> Zeitüberschreitung <dt>0xa0040202</dt> </dl>                           | Der Vorgang wurde nicht rechtzeitig beendet.<br/>                           |
| <dl> <dt>**VM \_ E \_ ADDITIONS \_ - \_ Funktion \_ nicht**</dt> " <dt>uxa0040505</dt> " </dl>       | Das Feature "Integrations Komponenten" ist auf diesem virtuellen Computer nicht installiert.<br/> |
| <dl> <dt>**VM \_ E \_ - \_ VM \_ führt**</dt> <dt>0xa0040206</dt> nicht aus </dl>                     | Der virtuelle Computer (VM) muss für diesen Vorgang ausgeführt werden.<br/>                 |
| <dl> <dt>**VM \_ E \_ VM \_ unbekannt**</dt> <dt>0xa0040207</dt> </dl>                          | Die Konfiguration ist unbekannt.<br/>                                                |



 

## <a name="remarks"></a>Bemerkungen

`HRESULT_FROM_WIN32(ERROR_NO_SUCH_LOGON_SESSION)` (0x80070520) wird durch die [**Error**](ivmtask-error.md) -Eigenschaft des zurückgegebenen [**ivmtask**](ivmtask.md) -Objekts zurückgegeben. es sind keine Anmelde Sitzungen im Gast Betriebssystem vorhanden.

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

 

