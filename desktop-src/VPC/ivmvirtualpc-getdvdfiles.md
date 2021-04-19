---
title: Ivmvirtualpc getdvdfiles-Methode (vpccominterfaces. h)
description: Ruft ein Array bekannter DVD-Dateien ab.
ms.assetid: 9fe2191f-c5c0-464d-a190-29b2aba69682
keywords:
- Getdvdfiles-Methode Virtual PC
- Getdvdfiles-Methode Virtual PC, ivmvirtualpc-Schnittstelle
- Ivmvirtualpc Interface Virtual PC, getdvdfiles-Methode
topic_type:
- apiref
api_name:
- IVMVirtualPC.GetDVDFiles
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a91d7f0d65d1f62feb21d41bd9b27bf6ce112ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342643"
---
# <a name="ivmvirtualpcgetdvdfiles-method"></a>Ivmvirtualpc:: getdvdfiles-Methode

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Ruft ein Array bekannter DVD-Dateien ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetDVDFiles(
  [in]          VARIANT inAdditionalSearchPaths,
  [out, retval] VARIANT *outDVDFileList
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*inadditionalsearchpath* \[ in\]
</dt> <dd>

Diese Pfade werden zusammen mit den Pfaden durchsucht, die in der [**ivmvirtualpc:: SearchPath**](ivmvirtualpc-searchpaths.md) -Eigenschaft festgelegt sind.

</dd> <dt>

*outdvdfilelist* \[ Out, retval\]
</dt> <dd>

Ein Array von virtuellen DVD-Dateien, die in den angegebenen Suchpfaden gefunden werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode/-wert                                                                                                                                                                        | BESCHREIBUNG                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                              | Der Vorgang wurde durchgeführt.<br/>                                                        |
| <dl> <dt>**E \_ Zeiger**</dt> <dt>0x80004003</dt> </dl>                                | Der *outdvdfilelist* -Parameter ist **null**.<br/>                                          |
| <dl> <dt>**E \_ InvalidArg**</dt> <dt>0x80000003</dt> </dl>                             | Der *inadditionalsearchpath* -Parameter ist kein Array von Zeichen folgen.<br/>                  |
| <dl> <dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt> </dl>                        | Ein unerwarteter Fehler ist aufgetreten.<br/>                                                    |
| <dl> <dt>**VM \_ E \_ \_ Hardwarevirtualisierung \_ deaktiviert**</dt> <dt>0xa0040951</dt> </dl> | Der Prozessor bietet keine Unterstützung für hav-Erweiterungen (Hardware Beschleunigung Virtualization).<br/> |



 

## <a name="remarks"></a>Bemerkungen

Die Suchpfade, die zum Abrufen des Arrays von Dateien verwendet werden, [**enthalten zusätzlich zu**](ivmvirtualpc-searchpaths.md) den durch den *inadditionalsearchpath* -Parameter angegebenen und den installerspeicherort für das Integrations Komponenten Modul festgelegte.

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

 

