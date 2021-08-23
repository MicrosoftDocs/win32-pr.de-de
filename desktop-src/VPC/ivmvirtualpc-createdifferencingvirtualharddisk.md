---
title: IVMVirtualPC CreateDifferencingVirtualHardDisk-Methode (VPCCOMInterfaces.h)
description: Erstellt eine differenzierende virtuelle Festplatte.
ms.assetid: 6a33aa6f-a0e8-45d8-bdc1-0864561db162
keywords:
- CreateDifferencingVirtualHardDisk-Methode Virtueller PC
- CreateDifferencingVirtualHardDisk-Methode Virtueller PC, IVMVirtualPC-Schnittstelle
- IVMVirtualPC-Schnittstelle Virtueller PC , CreateDifferencingVirtualHardDisk-Methode
topic_type:
- apiref
api_name:
- IVMVirtualPC.CreateDifferencingVirtualHardDisk
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b065d7b1d7a5f5f21aa0120b58d4ca2dc9177d0a48f6b2389365ee37811883c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119394420"
---
# <a name="ivmvirtualpccreatedifferencingvirtualharddisk-method"></a>IVMVirtualPC::CreateDifferencingVirtualHardDisk-Methode

\[Windows Der virtuelle PC ist ab Windows 8 nicht mehr für die Verwendung verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Erstellt eine differenzierende virtuelle Festplatte.

## <a name="syntax"></a>Syntax


```C++
HRESULT CreateDifferencingVirtualHardDisk(
  [in]          BSTR    imagePath,
  [in]          BSTR    parentPath,
  [out, retval] IVMTask **diskTask
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*imagePath* \[ In\]
</dt> <dd>

Der Pfad zur neuen Datenträgerimagedatei. Der enthaltende Ordner wird erstellt, wenn er nicht vorhanden ist.

</dd> <dt>

*parentPath* \[ In\]
</dt> <dd>

Der Pfad zur übergeordneten Datenträgerimagedatei.

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
| <dl> <dt>**HRESULT \_ VON \_ WIN32(FEHLERPFAD \_ \_ NICHT \_ GEFUNDEN)**</dt> <dt>0X80070003</dt> </dl> | Das System kann den durch den *imagePath-* oder *parentPath-Parameter* angegebenen Pfad nicht finden.<br/>                                                                                                                                             |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ INVALID \_ DRIVE)**</dt> <dt>0x8007000f</dt> </dl>   | Die durch den *imagePath-Parameter* angegebene Datei befindet sich auf einer CD-ROM oder DVD-ROM.<br/>                                                                                                                                                          |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ INVALID \_ NAME)**</dt> <dt>0x8007007b</dt> </dl>    | Der *imagePath-* oder *parentPath-Parameter* enthält ein ungültiges Zeichen (eines von " \* ?:<>/ \| "").<br/>                                                                                                                                |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ BAD \_ PATHNAME)**</dt> <dt>0x800700a1</dt> </dl>    | Sowohl der *imagePath-Parameter* als auch der *parentPath-Parameter* geben einen leeren oder relativen Pfad an. Mindestens einer der Parameter muss ein absoluter Pfad sein.<br/>                                                                                       |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ BUFFER \_ OVERFLOW)**</dt> <dt>0x8007006f</dt> </dl> | Der durch die *parameter imagePath* oder *parentPath* angegebene Pfad ist zu lang. Die Länge des Pfads muss kleiner als 260 Zeichen sein.<br/>                                                                                              |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ ALREADY \_ EXISTS)**</dt> <dt>0x800700b7</dt> </dl>  | Die Datei, auf die vom *imagePath-Parameter* verwiesen wird, ist bereits vorhanden.<br/>                                                                                                                                                                    |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ DISK \_ FULL)**</dt> <dt>0x80070070</dt> </dl>       | Das dynamisch erweiterbare virtuelle Festplattenimage benötigt mindestens 8 MB freien Speicherplatz auf dem Hostvolume.<br/>                                                                                                                                      |
| <dl> <dt>**VM \_ E \_ IMAGE SIZE TOO \_ \_ \_ LARGE**</dt> <dt>0xA0040683</dt> </dl>                | Die *Parametergröße* muss kleiner als 2.088.960 MB sein. Wenn das Format FAT16 ist, muss die Größe kleiner als 2.000 MB sein.<br/>                                                                                                                   |
| <dl> <dt>**VM \_ E \_ IMAGE SIZE TOO \_ \_ \_ SMALL**</dt> <dt>0xA0040684</dt> </dl>                | Unformatierte und FAT16-formatierte virtuelle Festplattenimages müssen mindestens 3 MB groß sein. Fat32-formatierte virtuelle Festplattenimages müssen mindestens 514 MB groß sein.<br/>                                                                                   |
| <dl> <dt>**VM \_ E \_ FILE TOO LARGE FOR \_ \_ \_ \_ VOLUME**</dt> <dt>0xA0040679</dt> </dl>          | Das Hostvolume kann eine Datei dieser Größe nicht unterstützen, wenn das dynamisch erweiterbare image der virtuellen Festplatte bis zum vollständigen Grenzwert erweitert wird. Die maximale Dateigröße für ein FAT32-Volume beträgt 4 GB. Die maximale Dateigröße für ein FAT16-Volume beträgt 2 GB.<br/> |
| <dl> <dt>**VM \_ HERUNTERFAHREN \_ \_ DER \_ E-APP**</dt> <dt>0xA0040209</dt> </dl>                    | Die virtuelle Festplatte kann nicht erstellt werden, nachdem das Herunterfahren der Anwendung gestartet wurde.<br/>                                                                                                                                            |
| <dl> <dt>**VM \_ E \_ HARDWARE \_ VIRTUALIZATION \_ DISABLED**</dt> <dt>0xA0040951</dt> </dl>     | Der Prozessor unterstützt keine HAV-Erweiterungen (Hardware Accelerated Virtualization).<br/>                                                                                                                                                |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>                            | Ein unerwarteter Fehler ist aufgetreten.<br/>                                                                                                                                                                                                   |



 

## <a name="remarks"></a>Hinweise

Obwohl *imagePath* oder *parentPath* ein relativer Pfad sein kann, muss mindestens einer davon ein absoluter Pfad sein. Wenn ein Pfadparameter ein relativer Pfad ist, wird davon ausgegangen, dass er relativ zum anderen Pfadparameter ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Product (Produkt)<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualPC ist als 236ba0d9-a24a-4292-a132-27c1421dfd01 definiert.<br/>               |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IVMVirtualPC**](ivmvirtualpc.md)
</dt> </dl>

 

