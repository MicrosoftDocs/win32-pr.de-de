---
title: Ivmvirtualmachine removeharddiskconnection-Methode (vpccominterfaces. h)
description: Entfernt die angegebene Festplatten Verbindung von der virtuellen Maschine.
ms.assetid: d31f2442-aae4-4987-9188-fd32778604a1
keywords:
- Removeharddiskconnection-Methode Virtual PC
- Removeharddiskconnection-Methode Virtual PC, ivmvirtualmachine-Schnittstelle
- Ivmvirtualmachine Interface Virtual PC, removeharddiskconnection-Methode
topic_type:
- apiref
api_name:
- IVMVirtualMachine.RemoveHardDiskConnection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62a9bbf8b3aac0dd35c8390343c20a1b67b59101
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391954"
---
# <a name="ivmvirtualmachineremoveharddiskconnection-method"></a>Ivmvirtualmachine:: removeharddiskconnection-Methode

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Entfernt die angegebene Festplatten Verbindung von der virtuellen Maschine.

## <a name="syntax"></a>Syntax


```C++
HRESULT RemoveHardDiskConnection(
  [in] IVMHardDiskConnection *hardDiskConnection
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*harddiskconnection* \[ in\]
</dt> <dd>

Ein [**ivmharddiskconnection**](ivmharddiskconnection.md) -Objekt, das die zu entfernende Festplatten Verbindung darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode/-wert                                                                                                                                                            | BESCHREIBUNG                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                  | Der Vorgang wurde durchgeführt.<br/>                              |
| <dl> <dt>**E \_ Zeiger**</dt> <dt>0x80004003</dt> </dl>                    | Der-Parameter ist **null**.<br/>                                 |
| <dl> <dt>**VM \_ E \_ VM \_ unbekannt**</dt> <dt>0xa0040207</dt> </dl>            | Die Konfiguration ist unbekannt.<br/>                              |
| <dl> <dt>**VM \_ E- \_ VM wird \_ ausgeführt \_ oder \_**</dt> <dt>0xa004020b</dt> gespeichert </dl> | Der virtuelle Computer befindet sich im Zustand "wird ausgeführt" oder "gespeichert".<br/>        |
| <dl> <dt>**VM \_ E \_ Laufwerk \_ ungültige**</dt> <dt>0xa0040502</dt> </dl>         | Das angegebene Laufwerk ist nicht mit diesem Busstandort verbunden.<br/> |
| <dl> <dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt> </dl>            | Ein unerwarteter Fehler ist aufgetreten.<br/>                          |



 

## <a name="remarks"></a>Bemerkungen

Sie können eine vorhandene Festplatten Verbindung nur von einem beendeten virtuellen Computer entfernen. Eine Liste der Verbindungen, die derzeit an den virtuellen Computer angefügt sind, wird durch Aufzählen der [**harddiskconnections**](ivmvirtualmachine-harddiskconnections.md) -Eigenschaft abgerufen.

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

 

