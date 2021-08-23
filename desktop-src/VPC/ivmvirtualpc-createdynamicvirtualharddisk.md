---
title: IVMVirtualPC CreateDynamicVirtualHardDisk-Methode (VPCCOMInterfaces.h)
description: Erstellt eine dynamische Größenänderung der virtuellen Festplatte.
ms.assetid: 2373ac41-c4c4-44c6-93e1-92814cd40b81
keywords:
- CreateDynamicVirtualHardDisk-Methode Virtueller PC
- CreateDynamicVirtualHardDisk-Methode Virtueller PC, IVMVirtualPC-Schnittstelle
- IVMVirtualPC-Schnittstelle Virtueller PC , CreateDynamicVirtualHardDisk-Methode
topic_type:
- apiref
api_name:
- IVMVirtualPC.CreateDynamicVirtualHardDisk
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6de505f2e8b47bc36b7537a3abcdab1f07e7551a8c5ed9caee9aed100288df51
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998650"
---
# <a name="ivmvirtualpccreatedynamicvirtualharddisk-method"></a>IVMVirtualPC::CreateDynamicVirtualHardDisk-Methode

\[Windows Der virtuelle PC ist ab Windows 8 nicht mehr für die Verwendung verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Erstellt eine dynamische Größenänderung der virtuellen Festplatte.

## <a name="syntax"></a>Syntax


```C++
HRESULT CreateDynamicVirtualHardDisk(
  [in]          BSTR    imagePath,
  [in]          long    size,
  [out, retval] IVMTask **diskTask
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*imagePath* \[ In\]
</dt> <dd>

Der vollständige Pfad zur neuen Datenträgerimagedatei. Der enthaltende Ordner wird erstellt, wenn er nicht vorhanden ist.

</dd> <dt>

*Size (Größe)* \[ In\]
</dt> <dd>

Die Größe des Bilds in Megabyte. Dieser Wert kann höchstens 2.088.960 MB (2.040 GB) betragen.

</dd> <dt>

*diskTask* \[ out, retval\]
</dt> <dd>

Ein [**IVMTask-Objekt,**](ivmtask.md) das zum Nachverfolgen der Imageerstellung verwendet wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode/-wert                                                                                                                                                                            | BESCHREIBUNG                                                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                  | Der Vorgang wurde durchgeführt.<br/>                                                                                                                                                                                                       |
| <dl> <dt>**E \_ POINTER**</dt> <dt>0x80004003</dt> </dl>                                    | Ein Parameter ist **NULL.**<br/>                                                                                                                                                                                                            |
| <dl> <dt>**E \_ INVALIDARG-0x80000003**</dt> <dt></dt> </dl>                                 | Der *size-Parameter* ist kleiner oder gleich 0.<br/>                                                                                                                                                                                    |
| <dl> <dt>**HRESULT \_ VON \_ WIN32(FEHLERPFAD \_ \_ NICHT \_ GEFUNDEN)**</dt> <dt>0X80070003</dt> </dl> | Das System kann den vom *imagePath-Parameter* angegebenen Pfad nicht finden.<br/>                                                                                                                                                             |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ INVALID \_ DRIVE)**</dt> <dt>0x8007000f</dt> </dl>   | Die durch den *imagePath-Parameter* angegebene Datei befindet sich auf einer CD-ROM oder DVD-ROM.<br/>                                                                                                                                                          |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ INVALID \_ NAME)**</dt> <dt>0x8007007b</dt> </dl>    | Der *imagePath-Parameter* enthält ein ungültiges Zeichen (eines von " \* ?:<>\| /"").<br/>                                                                                                                                                |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ BAD \_ PATHNAME)**</dt> <dt>0x800700a1</dt> </dl>    | Der *imagePath-Parameter* gibt einen leeren oder relativen Pfad an. Mindestens einer der Parameter muss ein absoluter Pfad sein.<br/>                                                                                                        |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ BUFFER \_ OVERFLOW)**</dt> <dt>0x8007006f</dt> </dl> | Der vom *imagePath-Parameter* angegebene Pfad ist zu lang. Die Länge des Pfads muss kleiner als 260 Zeichen sein.<br/>                                                                                                               |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ ALREADY \_ EXISTS)**</dt> <dt>0x800700b7</dt> </dl>  | Die Datei, auf die vom *imagePath-Parameter* verwiesen wird, ist bereits vorhanden.<br/>                                                                                                                                                                    |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ DISK \_ FULL)**</dt> <dt>0x80070070</dt> </dl>       | Das dynamisch erweiterbare virtuelle Festplattenimage benötigt mindestens 8 MB freien Speicherplatz auf dem Hostvolume.<br/>                                                                                                                                      |
| <dl> <dt>**VM \_ E \_ IMAGE SIZE TOO \_ \_ \_ LARGE**</dt> <dt>0xA0040683</dt> </dl>                | Die *Parametergröße* muss kleiner als 2.088.960 MB sein. Wenn das Format FAT16 ist, muss die Größe kleiner als 2.000 MB sein.<br/>                                                                                                                   |
| <dl> <dt>**VM \_ E \_ IMAGE SIZE TOO \_ \_ \_ SMALL**</dt> <dt>0xA0040684</dt> </dl>                | Unformatierte und FAT16-formatierte virtuelle Festplattenimages müssen mindestens 3 MB groß sein. Fat32-formatierte virtuelle Festplattenimages müssen mindestens 514 MB groß sein.<br/>                                                                                   |
| <dl> <dt>**VM \_ E \_ FILE TOO LARGE FOR \_ \_ \_ \_ VOLUME**</dt> <dt>0xA0040679</dt> </dl>          | Das Hostvolume kann eine Datei dieser Größe nicht unterstützen, wenn das dynamisch erweiterbare image der virtuellen Festplatte bis zum vollständigen Grenzwert erweitert wird. Die maximale Dateigröße für ein FAT32-Volume beträgt 4 GB. Die maximale Dateigröße für ein FAT16-Volume beträgt 2 GB.<br/> |
| <dl> <dt>**VM \_ HERUNTERFAHREN \_ \_ DER \_ E-APP**</dt> <dt>0xA0040209</dt> </dl>                    | Die virtuelle Festplatte kann nicht erstellt werden, nachdem das Herunterfahren der Anwendung gestartet wurde.<br/>                                                                                                                                            |
| <dl> <dt>**VM \_ E \_ HARDWARE \_ VIRTUALIZATION \_ DISABLED**</dt> <dt>0xA0040951</dt> </dl>     | Der Prozessor unterstützt keine HAV-Erweiterungen (Hardware Accelerated Virtualization).<br/>                                                                                                                                                |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>                            | Ein unerwarteter Fehler ist aufgetreten.<br/>                                                                                                                                                                                                   |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Product (Produkt)<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualPC ist als 236ba0d9-a24a-4292-a132-27c1421dfd01 definiert.<br/>               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IVMVirtualPC**](ivmvirtualpc.md)
</dt> </dl>

 

