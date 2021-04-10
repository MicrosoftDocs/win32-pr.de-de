---
title: Ivmvirtualpc-Methode "deatefixedvirtualharddisk" (vpccominterfaces. h)
description: Erstellt eine virtuelle Festplatte mit fester Größe.
ms.assetid: c58a7f2c-efd7-4a39-9ce5-617baa82084b
keywords:
- Methode "" für den virtuellen PC
- Methode "kreatefixedvirtualharddisk" Virtual PC, ivmvirtualpc
- Ivmvirtualpc Interface Virtual PC, Methode "kreatefixedvirtualharddisk"
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
ms.openlocfilehash: 2c1c260611ba3a8b55f87f23d0957c53a304a471
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103959"
---
# <a name="ivmvirtualpccreatefixedvirtualharddisk-method"></a>Ivmvirtualpc:: deatefixedvirtualharddisk-Methode

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

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

*ImagePath* \[ in\]
</dt> <dd>

Der vollständige Pfad zur neuen Datenträger Image Datei. Der enthaltende Ordner wird erstellt, wenn er nicht vorhanden ist.

</dd> <dt>

*Größe* \[ in\]
</dt> <dd>

Die Größe des Bilds in Megabyte. Die maximale Größe beträgt 2.088.960 MB (2040gb).

</dd> <dt>

*disktask* \[ Out, retval\]
</dt> <dd>

Ein [**ivmtask**](ivmtask.md) -Objekt, das zum Nachverfolgen der Image Erstellung verwendet wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode/-wert                                                                                                                                                                            | BESCHREIBUNG                                                                                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                  | Der Vorgang wurde durchgeführt.<br/>                                                                                                                        |
| <dl> <dt>**E \_ Zeiger**</dt> <dt>0x80004003</dt> </dl>                                    | Ein Parameter ist **null**.<br/>                                                                                                                             |
| <dl> <dt>**E \_ InvalidArg**</dt> <dt>0x80000003</dt> </dl>                                 | Der *size* -Parameter ist kleiner oder gleich 0 (null).<br/>                                                                                                     |
| <dl> <dt>**HRESULT \_ FROM \_ Win32 (Fehler \_ Pfad \_ nicht \_ gefunden)**</dt> <dt>0x80070003</dt> </dl> | Das System kann den durch den *ImagePath* -Parameter angegebenen Pfad nicht finden.<br/>                                                                              |
| <dl> <dt>**HRESULT \_ Von \_ Win32 (Fehler \_ ungültiges \_ Laufwerk)**</dt> <dt>0x8007000f</dt> </dl>   | Die durch den *ImagePath* -Parameter angegebene Datei befindet sich auf einer CD-ROM oder DVD-ROM.<br/>                                                                           |
| <dl> <dt>**HRESULT \_ Von \_ Win32 ( \_ ungültiger \_ Name)**</dt> <dt>0x8007007b</dt> </dl>    | Der *ImagePath* -Parameter enthält ein ungültiges Zeichen (eines von " \* ?: <>/ \| " ").<br/>                                                                 |
| <dl> <dt>**HRESULT \_ FROM \_ Win32 (Error ungültiger \_ \_ Pfadname)**</dt> <dt>0x800700a1</dt> </dl>    | Sowohl der *ImagePath* -Parameter gibt einen leeren als auch einen relativen Pfad an. Mindestens einer der Parameter muss ein absoluter Pfad sein.<br/>                         |
| <dl> <dt>**HRESULT \_ Von \_ Win32 (Fehler \_ Puffer \_ Überlauf)**</dt> <dt>0x8007006f</dt> </dl> | Der durch den *ImagePath* -Parameter angegebene Pfad ist zu lang. Die Länge des Pfads muss kleiner als der **Maximale \_ Pfad** (260) sein.<br/>                |
| <dl> <dt>**HRESULT \_ Von \_ Win32 (Fehler \_ bereits \_ vorhanden)**</dt> <dt>0x800700b7</dt> </dl>  | Die Datei, auf die der *ImagePath* -Parameter verweist, ist bereits vorhanden.<br/>                                                                                     |
| <dl> <dt>**HRESULT \_ Von \_ Win32 (Fehler \_ \_**</dt> Datenträger voll) <dt>0x80070070</dt> </dl>       | Für das dynamisch erweiterbare virtuelle Festplatten Abbild sind mindestens 8 MB freier Speicherplatz auf dem Host Volume erforderlich.<br/>                                                       |
| <dl> <dt>**VM \_ E- \_ Abbild \_ Größe \_ zu \_ groß**</dt> <dt>0xa0040683</dt> </dl>                | Der *size* -Parameter muss kleiner als 2.088.960 MB sein. Wenn das Format "FAT16" ist, muss der *size* -Parameter kleiner als 2000 MB sein.<br/>                    |
| <dl> <dt>**VM \_ E- \_ Abbild \_ Größe \_ zu \_ klein**</dt> <dt>0xa0040684</dt> </dl>                | Nicht formatierte und FAT16 formatierte virtuelle Festplatten Abbilder müssen mindestens 3 MB groß sein. Auf FAT32 formatierte virtuelle Festplatten Abbilder müssen mindestens 514 MB groß sein.<br/>    |
| <dl> <dt>**VM \_ E- \_ Datei \_ zu \_ groß \_ für \_ Volume**</dt> <dt>0xa0040679</dt> </dl>          | Die Größe der Datei kann vom Hostvolume nicht unterstützt werden. Die maximale Dateigröße für ein FAT32-Volume beträgt 4 GB. Die maximale Dateigröße für ein FAT16-Volume beträgt 2 GB.<br/> |
| <dl> <dt>**VM \_ E \_ App \_ \_ herunter**</dt> fahren <dt>0xa0040209</dt> </dl>                    | Die virtuelle Festplatte kann nicht erstellt werden, nachdem das Herunterfahren der Anwendung gestartet wurde.<br/>                                                             |
| <dl> <dt>**VM \_ E \_ \_ Hardwarevirtualisierung \_ deaktiviert**</dt> <dt>0xa0040951</dt> </dl>     | Der Prozessor bietet keine Unterstützung für hav-Erweiterungen (Hardware Beschleunigung Virtualization).<br/>                                                                 |
| <dl> <dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt> </dl>                            | Ein unerwarteter Fehler ist aufgetreten.<br/>                                                                                                                    |



 

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

 

