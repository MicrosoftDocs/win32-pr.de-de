---
title: IVMVirtualPC GetHardDisk-Methode (VPCCOMInterfaces.h)
description: Ruft ein Objekt ab, das einer vorhandenen Datenträgerimagedatei entspricht.
ms.assetid: 648a3f8a-5114-4c14-b9a9-f175941333ab
keywords:
- GetHardDisk-Methode Virtueller PC
- GetHardDisk-Methode Virtueller PC, IVMVirtualPC-Schnittstelle
- IVMVirtualPC-Schnittstelle Virtueller PC, GetHardDisk-Methode
topic_type:
- apiref
api_name:
- IVMVirtualPC.GetHardDisk
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc57085662c62951032837db178888bac5cb4407b11d7777d2f165f7b9c5a100
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136583"
---
# <a name="ivmvirtualpcgetharddisk-method"></a>IVMVirtualPC::GetHardDisk-Methode

\[Windows Der virtuelle PC ist ab diesem Zeitraum nicht mehr Windows 8. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Ruft ein Objekt ab, das einer vorhandenen Datenträgerimagedatei entspricht.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetHardDisk(
  [in]          BSTR        imagePath,
  [out, retval] IVMHardDisk **hardDisk
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*imagePath* \[ In\]
</dt> <dd>

Der vollständige Pfad zu einer vorhandenen Datenträgerimagedatei.

</dd> <dt>

*hardDisk* \[ out, retval\]
</dt> <dd>

Ein [**IVMHardDisk-Objekt,**](ivmharddisk.md) das diesem Datenträgerimage entspricht.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode/-wert                                                                                                                                                                            | Beschreibung                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                  | Der Vorgang wurde durchgeführt.<br/>                                                                                         |
| <dl> <dt>**E \_ ZEIGER 0X80004003**</dt> <dt></dt> </dl>                                    | Der *imagePath-* oder *hardDisk-Parameter* ist **NULL.**<br/>                                                                  |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ FILE NOT \_ \_ FOUND)**</dt> <dt>0X80070002</dt> </dl> | Das System kann die durch den *imagePath-Parameter angegebene Datei nicht* finden.<br/>                                               |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ PATH NOT \_ \_ FOUND)**</dt> <dt>0x80070003</dt> </dl> | Das System kann den durch den *imagePath-Parameter angegebenen Pfad nicht* finden.<br/>                                               |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ INVALID \_ NAME)**</dt> <dt>0x8007007b</dt> </dl>    | Der *imagePath-Parameter* enthält ein ungültiges Zeichen (eines von " \* ?:<>/ \| "").<br/>                                  |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ BAD \_ PATHNAME)**</dt> <dt>0x800700a1</dt> </dl>    | Der *imagePath-Parameter* gibt einen leeren oder relativen Pfad an. Ein absoluter Pfad ist erforderlich.<br/>                          |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ BUFFER \_ OVERFLOW)**</dt> <dt>0x8007006f</dt> </dl> | Der durch den *imagePath-Parameter angegebene Pfad* ist zu lang. Die Länge des Pfads muss weniger als 260 Zeichen umfassen.<br/> |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>                            | Ein unerwarteter Fehler ist aufgetreten.<br/>                                                                                     |
| <dl> <dt>**VM \_ E \_ \_ HARDWAREVIRTUALISIERUNG \_ DEAKTIVIERT**</dt> <dt>0XA0040951</dt> </dl>     | Der Prozessor unterstützt keine HAV-Erweiterungen (Hardware Accelerated Virtualization).<br/>                                  |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Product (Produkt)<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualPC ist als 236ba0d9-a24a-4292-a132-27c1421dfd01 definiert.<br/>               |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IVMVirtualPC**](ivmvirtualpc.md)
</dt> </dl>

 

