---
title: Ivmvirtualpc-Methode "kreatedifferencingvirtualharddisk" (vpccominterfaces. h)
description: Erstellt eine differenzierende virtuelle Festplatte.
ms.assetid: 6a33aa6f-a0e8-45d8-bdc1-0864561db162
keywords:
- Methode "kreatedifferencingvirtualharddisk" Virtual PC
- "\"Kreatedifferencingvirtualharddisk\"-Methode Virtual PC, ivmvirtualpc-Schnittstelle"
- Ivmvirtualpc Interface Virtual PC, Methode "kreatedifferencingvirtualharddisk"
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
ms.openlocfilehash: b2bab178d64008b236988bfb723bd75a09a7edaa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106344093"
---
# <a name="ivmvirtualpccreatedifferencingvirtualharddisk-method"></a>Ivmvirtualpc:: kreatedifferencingvirtualharddisk-Methode

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

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

*ImagePath* \[ in\]
</dt> <dd>

Der Pfad zur neuen Datenträger Image Datei. Der enthaltende Ordner wird erstellt, wenn er nicht vorhanden ist.

</dd> <dt>

Element *Pfad* \[ in\]
</dt> <dd>

Der Pfad zur Datei für den übergeordneten Datenträger Image.

</dd> <dt>

*disktask* \[ Out, retval\]
</dt> <dd>

Ein [**ivmtask**](ivmtask.md) -Objekt, das zum Nachverfolgen der Image Erstellung verwendet wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode/-wert                                                                                                                                                                            | BESCHREIBUNG                                                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                  | Der Vorgang wurde durchgeführt.<br/>                                                                                                                                                                                                       |
| <dl> <dt>**E \_ Zeiger**</dt> <dt>0x80004003</dt> </dl>                                    | Ein Parameter ist **null**.<br/>                                                                                                                                                                                                            |
| <dl> <dt>**HRESULT \_ FROM \_ Win32 (Fehler \_ Pfad \_ nicht \_ gefunden)**</dt> <dt>0x80070003</dt> </dl> | Das System kann den durch den Parameter " *ImagePath* " oder " *Parameter Path"* angegebenen Pfad nicht finden.<br/>                                                                                                                                             |
| <dl> <dt>**HRESULT \_ Von \_ Win32 (Fehler \_ ungültiges \_ Laufwerk)**</dt> <dt>0x8007000f</dt> </dl>   | Die durch den *ImagePath* -Parameter angegebene Datei befindet sich auf einer CD-ROM oder DVD-ROM.<br/>                                                                                                                                                          |
| <dl> <dt>**HRESULT \_ Von \_ Win32 ( \_ ungültiger \_ Name)**</dt> <dt>0x8007007b</dt> </dl>    | Der Parameter " *ImagePath* " oder "Parameter *path* " enthält ein ungültiges Zeichen (" \* ?: <>/ \| " ").<br/>                                                                                                                                |
| <dl> <dt>**HRESULT \_ FROM \_ Win32 (Error ungültiger \_ \_ Pfadname)**</dt> <dt>0x800700a1</dt> </dl>    | Sowohl der *ImagePath* -Parameter als auch der Parameter *Parameter Path geben* einen leeren oder relativen Pfad an. Mindestens einer der Parameter muss ein absoluter Pfad sein.<br/>                                                                                       |
| <dl> <dt>**HRESULT \_ Von \_ Win32 (Fehler \_ Puffer \_ Überlauf)**</dt> <dt>0x8007006f</dt> </dl> | Der von den Parametern " *ImagePath* " oder "Parameter *path* " angegebene Pfad ist zu lang. Die Länge des Pfads muss weniger als 260 Zeichen umfassen.<br/>                                                                                              |
| <dl> <dt>**HRESULT \_ Von \_ Win32 (Fehler \_ bereits \_ vorhanden)**</dt> <dt>0x800700b7</dt> </dl>  | Die Datei, auf die der *ImagePath* -Parameter verweist, ist bereits vorhanden.<br/>                                                                                                                                                                    |
| <dl> <dt>**HRESULT \_ Von \_ Win32 (Fehler \_ \_**</dt> Datenträger voll) <dt>0x80070070</dt> </dl>       | Für das dynamisch erweiterbare virtuelle Festplatten Abbild sind mindestens 8 MB freier Speicherplatz auf dem Host Volume erforderlich.<br/>                                                                                                                                      |
| <dl> <dt>**VM \_ E- \_ Abbild \_ Größe \_ zu \_ groß**</dt> <dt>0xa0040683</dt> </dl>                | Die Parameter *Größe* muss kleiner als 2.088.960 MB sein. Wenn das Format "FAT16" ist, muss die Größe kleiner als 2000 MB sein.<br/>                                                                                                                   |
| <dl> <dt>**VM \_ E- \_ Abbild \_ Größe \_ zu \_ klein**</dt> <dt>0xa0040684</dt> </dl>                | Nicht formatierte und FAT16 formatierte virtuelle Festplatten Abbilder müssen mindestens 3 MB groß sein. Auf FAT32 formatierte virtuelle Festplatten Abbilder müssen mindestens 514 MB groß sein.<br/>                                                                                   |
| <dl> <dt>**VM \_ E- \_ Datei \_ zu \_ groß \_ für \_ Volume**</dt> <dt>0xa0040679</dt> </dl>          | Die Größe der Datei kann vom Hostvolume nicht unterstützt werden, wenn das Image der dynamisch erweiterbaren virtuellen Festplatte auf den vollständigen Grenzwert erweitert wird. Die maximale Dateigröße für ein FAT32-Volume beträgt 4 GB. Die maximale Dateigröße für ein FAT16-Volume beträgt 2 GB.<br/> |
| <dl> <dt>**VM \_ E \_ App \_ \_ herunter**</dt> fahren <dt>0xa0040209</dt> </dl>                    | Die virtuelle Festplatte kann nicht erstellt werden, nachdem das Herunterfahren der Anwendung gestartet wurde.<br/>                                                                                                                                            |
| <dl> <dt>**VM \_ E \_ \_ Hardwarevirtualisierung \_ deaktiviert**</dt> <dt>0xa0040951</dt> </dl>     | Der Prozessor bietet keine Unterstützung für hav-Erweiterungen (Hardware Beschleunigung Virtualization).<br/>                                                                                                                                                |
| <dl> <dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt> </dl>                            | Ein unerwarteter Fehler ist aufgetreten.<br/>                                                                                                                                                                                                   |



 

## <a name="remarks"></a>Bemerkungen

Obwohl *es sich bei* entweder um *ImagePath* oder um einen relativen Pfad handeln kann, muss mindestens einer der Pfade ein absoluter Pfad sein. Wenn ein Pfad Parameter ein relativer Pfad ist, wird davon ausgegangen, dass er relativ zum anderen path-Parameter ist.

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

 

