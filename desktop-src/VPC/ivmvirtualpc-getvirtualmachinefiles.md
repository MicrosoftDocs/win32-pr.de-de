---
title: Ivmvirtualpc getvirtualmachinefiles-Methode (vpccominterfaces. h)
description: Ruft ein Array bekannter Konfigurationsdateien für virtuelle Maschinen ab.
ms.assetid: 38771573-66fa-408a-95db-1281efdf8b73
keywords:
- Getvirtualmachinefiles-Methode virtueller PC
- Getvirtualmachinefiles-Methode Virtual PC, ivmvirtualpc-Schnittstelle
- Ivmvirtualpc Interface Virtual PC, getvirtualmachinefiles-Methode
topic_type:
- apiref
api_name:
- IVMVirtualPC.GetVirtualMachineFiles
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5d1fe248b76756b39846d181341278f669d2f5f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341227"
---
# <a name="ivmvirtualpcgetvirtualmachinefiles-method"></a>Ivmvirtualpc:: getvirtualmachinefiles-Methode

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Ruft ein Array bekannter Konfigurationsdateien für virtuelle Maschinen ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetVirtualMachineFiles(
  [in]          VARIANT      inAdditionalSearchPaths,
  [in]          VARIANT_BOOL inExcludedRegisteredVMs,
  [out, retval] VARIANT      *outVirtualMachineFileList
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*inadditionalsearchpath* \[ in\]
</dt> <dd>

Diese Pfade werden zusammen mit den Pfaden durchsucht, die in den Eigenschaften [**ivmvirtualpc:: SearchPath**](ivmvirtualpc-searchpaths.md) und [**ivmvirtualpc::D efaultvmconfigurationpath**](ivmvirtualpc-defaultvmconfigurationpath.md) festgelegt sind.

</dd> <dt>

*inexcluddregisteredvms* \[ in\]
</dt> <dd>

**True** , wenn registrierte virtuelle Computer aus dem Array ausgeschlossen werden sollen, wenn der *outvirtualmachinefilelist* -Parameter zurückgegeben wird, andernfalls **false** .

</dd> <dt>

*outvirtualmachinefilelist* \[ Out, retval\]
</dt> <dd>

Ein Array von Pfad Zeichenfolgen für die Konfigurationsdateien der virtuellen Maschine, die in den angegebenen Suchpfaden gefunden wurden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode/-wert                                                                                                                                                                        | BESCHREIBUNG                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                              | Der Vorgang wurde durchgeführt.<br/>                                                        |
| <dl> <dt>**E \_ Zeiger**</dt> <dt>0x80004003</dt> </dl>                                | Der *outvirtualmachinefilelist* -Parameter ist **null**.<br/>                               |
| <dl> <dt>**E \_ InvalidArg**</dt> <dt>0x80000003</dt> </dl>                             | Der *inadditionalsearchpath* -Parameter ist kein Array von Zeichen folgen.<br/>                  |
| <dl> <dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt> </dl>                        | Ein unerwarteter Fehler ist aufgetreten.<br/>                                                    |
| <dl> <dt>**VM \_ E \_ \_ Hardwarevirtualisierung \_ deaktiviert**</dt> <dt>0xa0040951</dt> </dl> | Der Prozessor bietet keine Unterstützung für hav-Erweiterungen (Hardware Beschleunigung Virtualization).<br/> |



 

## <a name="remarks"></a>Bemerkungen

Die Suchpfade, die zum Abrufen des Arrays von Konfigurationsdateien verwendet werden, enthalten diejenigen, die zuvor von [**ivmvirtualpc:: SearchPath**](ivmvirtualpc-searchpaths.md) und [**ivmvirtualpc::D efaultvmconfigurationpath**](ivmvirtualpc-defaultvmconfigurationpath.md) festgelegt wurden, zusätzlich zu den vom *inadditionalsearchpath* -Parameter angegebenen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Vpccominterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ ivmvirtualpc ist als 236ba0d9-a24a-4292-A132-27c1421dfd01 definiert.<br/>               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ivmvirtualpc**](ivmvirtualpc.md)
</dt> </dl>

 

