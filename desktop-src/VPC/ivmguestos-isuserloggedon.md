---
title: Ivmguestos isuserloggedon-Methode (vpccominterfaces. h)
description: Bestimmt, ob die angeforderte Sitzung vorhanden ist.
ms.assetid: 28035e30-023a-4ec2-88ef-43fe22f6d14e
keywords:
- Isuserloggedon-Methode virtueller PC
- Isuserloggedon-Methode Virtual PC, ivmguestos-Schnittstelle
- Ivmguestos Interface Virtual PC, isuserloggedon-Methode
topic_type:
- apiref
api_name:
- IVMGuestOS.IsUserLoggedOn
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4eeb0482d7d3ac45b67a863948526b57d6c6e412
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340971"
---
# <a name="ivmguestosisuserloggedon-method"></a>Ivmguestos:: isuserloggedon-Methode

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Bestimmt, ob die angeforderte Sitzung vorhanden ist.

## <a name="syntax"></a>Syntax


```C++
HRESULT IsUserLoggedOn(
  [in]          long         inRailSession,
  [out, retval] VARIANT_BOOL *outSessionPresent
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*inrailsession* \[ in\]
</dt> <dd>

Legen Sie für eine Rail-Sitzung auf 0 oder für eine RDP-Sitzung den Wert 1 fest.

</dd> <dt>

*outsessionpresent* \[ Out, retval\]
</dt> <dd>

Auf **Variant \_ true** festgelegt, wenn die Sitzung vorhanden ist, andernfalls **\_ false** .

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode/-wert                                                                                                                                                                       | BESCHREIBUNG                                                                |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                             | Der Vorgang wurde durchgeführt.<br/>                                   |
| <dl> <dt>**E \_ Zeiger**</dt> <dt>0x80004003</dt> </dl>                               | Der-Parameter ist **null**.<br/>                                      |
| <dl> <dt>**E \_ InvalidArg**</dt> <dt>0x80000003</dt> </dl>                            | Der *outsessionpresent* -Parameter ist ungültig oder **null**.<br/>  |
| <dl> <dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt> </dl>                       | Ein unerwarteter Fehler ist aufgetreten.<br/>                               |
| <dl> <dt>**HRESULT \_ Von \_ Win32 (Error \_ outo-Memory)**</dt> <dt>0x8007000E</dt> </dl> | Es ist nicht genügend Arbeitsspeicher verfügbar, um diese Anforderung abzuschließen.<br/>  |
| <dl> <dt>**VM \_ E \_ \_**</dt> Zeitüberschreitung <dt>0xa0040202</dt> </dl>                        | Der Vorgang wurde nicht rechtzeitig beendet.<br/>              |
| <dl> <dt>**VM \_ E \_ - \_ VM \_ führt**</dt> <dt>0xa0040206</dt> nicht aus </dl>                  | Der virtuelle Computer (VM) muss für diesen Vorgang ausgeführt werden.<br/>    |
| <dl> <dt>**VM \_ E \_ ADDITIONS \_ - \_ Funktion \_ nicht**</dt> " <dt>uxa0040505</dt> " </dl>    | Das Feature "Integrations Komponenten" ist auf dieser VM nicht installiert.<br/> |
| <dl> <dt>**VM \_ E- \_ VM \_ angeh**</dt> alten <dt>0xa00400507</dt> </dl>                       | Der virtuelle Computer wurde angehalten.<br/>                                               |



 

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

 

