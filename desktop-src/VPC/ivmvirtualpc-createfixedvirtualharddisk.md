---
title: IVMVirtualPC CreateFixedVirtualHardDisk-Methode (VPCCOMInterfaces.h)
description: Erstellt eine virtuelle Festplatte mit fester Größe.
ms.assetid: c58a7f2c-efd7-4a39-9ce5-617baa82084b
keywords:
- CreateFixedVirtualHardDisk-Methode Virtueller PC
- CreateFixedVirtualHardDisk-Methode Virtual PC, IVMVirtualPC-Schnittstelle
- IVMVirtualPC-Schnittstelle Virtueller PC, CreateFixedVirtualHardDisk-Methode
topic_type:
- apiref
api_name:
- IVMVirtualPC.CreateFixedVirtualHardDisk
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 342fe173b8948fe1f445d4cf626602347fa845c914c6525d592069191062b3fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119056598"
---
# <a name="ivmvirtualpccreatefixedvirtualharddisk-method"></a>IVMVirtualPC::CreateFixedVirtualHardDisk-Methode

\[Windows Der virtuelle PC ist ab diesem Zeitraum nicht mehr Windows 8. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Erstellt eine virtuelle Festplatte mit fester Größe.

## <a name="syntax"></a>Syntax


```C++
HRESULT CreateFixedVirtualHardDisk(
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

*size* \[ In\]
</dt> <dd>

Die Größe des Bilds in Megabyte. Die maximale Größe beträgt 2.088.960 MB (2040 GB).

</dd> <dt>

*diskTask* \[ out, retval\]
</dt> <dd>

Ein [**IVMTask-Objekt,**](ivmtask.md) das zum Nachverfolgen der Erstellung des Images verwendet wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode/-wert                                                                                                                                                                            | Beschreibung                                                                                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                  | Der Vorgang wurde durchgeführt.<br/>                                                                                                                        |
| <dl> <dt>**E \_ ZEIGER 0X80004003**</dt> <dt></dt> </dl>                                    | Ein Parameter ist **NULL.**<br/>                                                                                                                             |
| <dl> <dt>**E \_ INVALIDARG-0x80000003**</dt> <dt></dt> </dl>                                 | Der *size-Parameter* ist kleiner oder gleich 0.<br/>                                                                                                     |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ PATH NOT \_ \_ FOUND)**</dt> <dt>0x80070003</dt> </dl> | Das System kann den durch den *imagePath-Parameter angegebenen Pfad nicht* finden.<br/>                                                                              |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ INVALID \_ DRIVE)**</dt> <dt>0X8007000F</dt> </dl>   | Die durch den *imagePath-Parameter angegebene Datei* befindet sich auf einer CD-ROM oder DVD-ROM.<br/>                                                                           |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ INVALID \_ NAME)**</dt> <dt>0x8007007b</dt> </dl>    | Der *imagePath-Parameter* enthält ein ungültiges Zeichen (eines von " \* ?:<>/ \| "").<br/>                                                                 |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ BAD \_ PATHNAME)**</dt> <dt>0x800700a1</dt> </dl>    | Der *imagePath-Parameter* gibt einen leeren oder relativen Pfad an. Mindestens einer der Parameter muss ein absoluter Pfad sein.<br/>                         |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ BUFFER \_ OVERFLOW)**</dt> <dt>0x8007006f</dt> </dl> | Der durch den *imagePath-Parameter angegebene Pfad* ist zu lang. Die Länge des Pfads muss kleiner als **MAX \_ PATH** (260) Zeichen sein.<br/>                |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ ALREADY \_ EXISTS)**</dt> <dt>0X800700B7</dt> </dl>  | Die Datei, auf die der *imagePath-Parameter* verweist, ist bereits vorhanden.<br/>                                                                                     |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ DISK \_ FULL)**</dt> <dt>0x80070070</dt> </dl>       | Das dynamisch erweiternde Image der virtuellen Festplatte benötigt mindestens 8 MB freien Speicherplatz auf dem Host-Volume.<br/>                                                       |
| <dl> <dt>**VM \_ E \_ \_ BILDGRÖßE \_ ZU \_ GROß**</dt> <dt>0XA0040683</dt> </dl>                | Der *size-Parameter* muss kleiner als 2.088.960 MB sein. Wenn das Format FAT16 ist, muss der *Size-Parameter* kleiner als 2000 MB sein.<br/>                    |
| <dl> <dt>**VM \_ E \_ \_ BILDGRÖßE \_ ZU \_ KLEIN**</dt> <dt>0XA0040684</dt> </dl>                | Images von unformatierten und FAT16-formatierten virtuellen Festplatten müssen mindestens 3 MB groß sein. IMAGES virtueller Festplatten im FAT32-Format müssen mindestens 514 MB groß sein.<br/>    |
| <dl> <dt>**VM \_ \_E-DATEI ZU GROß FÜR VOLUME \_ \_ \_ \_ 0XA0040679**</dt> <dt></dt> </dl>          | Das Host-Volume kann eine Datei dieser Größe nicht unterstützen. Die maximale Dateigröße für ein FAT32-Volume beträgt 4 GB. Die maximale Dateigröße für ein FAT16-Volume beträgt 2 GB.<br/> |
| <dl> <dt>**VM \_ \_ \_ E-APP WIRD \_ HERUNTERGEFAHREN**</dt> <dt>0XA0040209</dt> </dl>                    | Die virtuelle Festplatte kann nicht erstellt werden, nachdem die Anwendung heruntergefahren wurde.<br/>                                                             |
| <dl> <dt>**VM \_ E \_ \_ HARDWAREVIRTUALISIERUNG \_ DEAKTIVIERT**</dt> <dt>0XA0040951</dt> </dl>     | Der Prozessor unterstützt keine HAV-Erweiterungen (Hardware Accelerated Virtualization).<br/>                                                                 |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>                            | Ein unerwarteter Fehler ist aufgetreten.<br/>                                                                                                                    |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualPC ist als 236ba0d9-a24a-4292-a132-27c1421dfd01 definiert.<br/>               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IVMVirtualPC**](ivmvirtualpc.md)
</dt> </dl>

 

