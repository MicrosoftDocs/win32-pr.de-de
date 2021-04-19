---
title: Ivmguestos getosversioninfo-Methode (vpccominterfaces. h)
description: Ruft Versionsinformationen für das Gast Betriebssystem ab, das auf dem virtuellen Computer ausgeführt wird.
ms.assetid: 1f9d749f-6007-466d-9df9-71c6a72e8112
keywords:
- Getosversioninfo-Methode Virtual PC
- Getosversioninfo-Methode Virtual PC, ivmguestos-Schnittstelle
- Ivmguestos Interface Virtual PC, getosversioninfo-Methode
topic_type:
- apiref
api_name:
- IVMGuestOS.GetOsVersionInfo
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ec0c0c2516a8ef16a3d9d9c6c4178abb31bd52f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346337"
---
# <a name="ivmguestosgetosversioninfo-method"></a>Ivmguestos:: getosversioninfo-Methode

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Ruft Versionsinformationen für das Gast Betriebssystem ab, das auf dem virtuellen Computer (VM) ausgeführt wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetOsVersionInfo(
  [out, retval] GUESTOSVERSIONINFOEX **guestOsVersionInfo
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*guestosversioninfo* \[ Out, retval\]
</dt> <dd>

Ein Zeiger auf eine [**guestosversioninfoex**](guestosversioninfoex.md) -Struktur.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode/-wert                                                                                                                                                                       | BESCHREIBUNG                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                             | Der Vorgang wurde durchgeführt.<br/>                                  |
| <dl> <dt>**E \_ Zeiger**</dt> <dt>0x80004003</dt> </dl>                               | Der-Parameter ist **null**.<br/>                                     |
| <dl> <dt>**HRESULT \_ Von \_ Win32 (Error \_ outo-Memory)**</dt> <dt>0x8007000E</dt> </dl> | Es ist nicht genügend Arbeitsspeicher verfügbar, um diese Anforderung abzuschließen.<br/> |
| <dl> <dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt> </dl>                       | Ein unerwarteter Fehler ist aufgetreten.<br/>                              |
| <dl> <dt>**VM \_ E \_ - \_ VM \_ führt**</dt> <dt>0xa0040206</dt> nicht aus </dl>                  | Der virtuelle Computer wird nicht ausgeführt.<br/>                                         |
| <dl> <dt>**VM \_ E \_ ADDITIONS \_ - \_ Funktion \_ nicht**</dt> " <dt>uxa0040505</dt> " </dl>    | Integrations Komponenten sind auf diesem virtuellen Computer nicht installiert.<br/>           |



 

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

 

