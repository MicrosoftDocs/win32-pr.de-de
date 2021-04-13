---
title: Ivmvirtualmachine mergeundodisks-Methode (vpccominterfaces. h)
description: Führt die virtuellen Rückgängig-Datenträger zusammen.
ms.assetid: 6445b097-220e-48c4-9a7b-1139ca7b3338
keywords:
- Mergeundodisks-Methode virtueller PC
- Mergeundodisks-Methode Virtual PC, ivmvirtualmachine-Schnittstelle
- Ivmvirtualmachine Interface Virtual PC, mergeundodisks-Methode
topic_type:
- apiref
api_name:
- IVMVirtualMachine.MergeUndoDisks
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48863bf998ebc02bac93aa9e74d8cdbe07265477
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341067"
---
# <a name="ivmvirtualmachinemergeundodisks-method"></a>Ivmvirtualmachine:: mergeundodisks-Methode

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Führt die virtuellen Rückgängig-Datenträger zusammen.

## <a name="syntax"></a>Syntax


```C++
HRESULT MergeUndoDisks(
  [out, retval] IVMTask **undoMergeTask
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*rückgängig machen* \[ Out, retval\]
</dt> <dd>

Ein [**ivmtask**](ivmtask.md) -Objekt, das zum Nachverfolgen der Image Erstellung verwendet wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode/-wert                                                                                                                                                                            | BESCHREIBUNG                                                                                                                             |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                  | Der Vorgang wurde durchgeführt.<br/>                                                                                                |
| <dl> <dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt> </dl>                            | Ein unerwarteter Fehler ist aufgetreten.<br/>                                                                                            |
| <dl> <dt>**E \_ Zeiger**</dt> <dt>0x80004003</dt> </dl>                                    | Der-Parameter ist **null**.<br/>                                                                                                   |
| <dl> <dt>**HRESULT \_ FROM \_ Win32 (Fehler \_ Pfad \_ nicht \_ gefunden)**</dt> <dt>0x80070003</dt> </dl> | Das System kann den vom *converteddiskimagepath* -Parameter angegebenen Pfad nicht finden, oder einer der übergeordneten Datenträger ist ungültig.<br/> |
| <dl> <dt>**E \_ AccessDenied**</dt> <dt>0x80070005</dt> </dl>                               | Der aktuelle Benutzer hat keinen ausreichenden Zugriff auf die übergeordnete Datei.<br/>                                                                 |
| <dl> <dt>**E \_ Handle**</dt> <dt>0x80070006</dt> </dl>                                     | Einer der übergeordneten Datenträger wird verwendet.<br/>                                                                                           |
| <dl> <dt>**VM \_ E \_ VM \_ unbekannt**</dt> <dt>0xa0040207</dt> </dl>                            | Die Konfiguration ist unbekannt.<br/>                                                                                                |
| <dl> <dt>**VM \_ E \_ VM \_**</dt> mit <dt>0xa0040500</dt> </dl>                            | Der virtuelle Computer wird ausgeführt.<br/>                                                                                              |
| <dl> <dt>**VM \_ E \_ - \_ Datei \_**</dt> schreibgeschützt <dt>0xa004067a</dt> </dl>                       | Das übergeordnete Element von virtuellen Rückgängig-Datenträgern ist als schreibgeschützt gekennzeichnet.<br/>                                                                     |
| <dl> <dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt> </dl>                            | Ein unerwarteter Fehler ist aufgetreten.<br/>                                                                                            |



 

## <a name="remarks"></a>Bemerkungen

' **Mergeundodisks** ' kann nicht aufgerufen werden, während der virtuelle Computer weiterhin ausgeführt wird. Verwenden Sie [**ivmvirtualmachine:: Save**](ivmvirtualmachine-save.md) , um den Status des virtuellen Computers vor dem Aufrufen von **mergeundodisks** zu speichern, oder [**ivmvirtualmachine:: Turnoff**](ivmvirtualmachine-turnoff.md) , um den virtuellen Computer zu deaktivieren, ohne zuvor seinen aktuellen Zustand zu speichern.

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

 

