---
title: IVMVirtualPC GetFloppyDiskImageType-Methode (VPCCOMInterfaces.h)
description: Ruft den Typ einer vorhandenen Diskettenimagedatei ab.
ms.assetid: 34956a0c-1da0-4968-9a6c-c114d7037da1
keywords:
- GetFloppyDiskImageType-Methode Virtueller PC
- GetFloppyDiskImageType-Methode Virtueller PC, IVMVirtualPC-Schnittstelle
- IVMVirtualPC-Schnittstelle Virtueller PC , GetFloppyDiskImageType-Methode
topic_type:
- apiref
api_name:
- IVMVirtualPC.GetFloppyDiskImageType
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 891e07da259acc8e2efa759d636ac203654700785586a20f879cf75165ab318e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118122329"
---
# <a name="ivmvirtualpcgetfloppydiskimagetype-method"></a>IVMVirtualPC::GetFloppyDiskImageType-Methode

\[Windows Der virtuelle PC ist ab Windows 8 nicht mehr für die Verwendung verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Ruft den Typ einer vorhandenen Diskettenimagedatei ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetFloppyDiskImageType(
  [in]          BSTR                  imagePath,
  [out, retval] VMFloppyDiskImageType *imageType
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*imagePath* \[ In\]
</dt> <dd>

Der vollständige Pfad zur Datenträgerimagedatei.

</dd> <dt>

*imageType* \[ out, retval\]
</dt> <dd>

Der Datenträgerimagetyp. Eine Liste der Werte finden Sie unter [**VMFloppyDiskImageType.**](vmfloppydiskimagetype.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode/-wert                                                                                                                                                                            | Beschreibung                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                  | Der Vorgang wurde durchgeführt.<br/>                                                                                         |
| <dl> <dt>**E \_ POINTER**</dt> <dt>0x80004003</dt> </dl>                                    | Der *imagePath-* oder *imageType-Parameter* ist **NULL.**<br/>                                                                 |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ FILE NOT \_ \_ FOUND)**</dt> <dt>0x80070002</dt> </dl> | Das System kann die durch den *imagePath-Parameter* angegebene Datei nicht finden.<br/>                                               |
| <dl> <dt>**HRESULT \_ VON \_ WIN32(FEHLERPFAD \_ \_ NICHT \_ GEFUNDEN)**</dt> <dt>0X80070003</dt> </dl> | Das System kann den vom *imagePath-Parameter* angegebenen Pfad nicht finden.<br/>                                               |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ INVALID \_ NAME)**</dt> <dt>0x8007007b</dt> </dl>    | Der *imagePath-Parameter* enthält ein ungültiges Zeichen (eines von " \* ?:<>/ \| "").<br/>                                  |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ BAD \_ PATHNAME)**</dt> <dt>0x800700a1</dt> </dl>    | Der *imagePath-Parameter* gibt einen leeren oder relativen Pfad an. Ein absoluter Pfad ist erforderlich.<br/>                          |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ BUFFER \_ OVERFLOW)**</dt> <dt>0x8007006f</dt> </dl> | Der vom *imagePath-Parameter* angegebene Pfad ist zu lang. Die Länge des Pfads muss kleiner als 260 Zeichen sein.<br/> |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>                            | Die von *imagePath* angegebene Datei ist kein Diskettenimage, oder es ist ein unerwarteter Fehler aufgetreten.<br/>                         |
| <dl> <dt>**VM \_ E \_ \_ HARDWAREVIRTUALISIERUNG \_ DEAKTIVIERT**</dt> <dt>0xA0040951</dt> </dl>     | Der Prozessor unterstützt keine HAV-Erweiterungen (Hardware Accelerated Virtualization).<br/>                                  |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualPC ist als 236ba0d9-a24a-4292-a132-27c1421dfd01 definiert.<br/>               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IVMVirtualPC**](ivmvirtualpc.md)
</dt> </dl>

 

