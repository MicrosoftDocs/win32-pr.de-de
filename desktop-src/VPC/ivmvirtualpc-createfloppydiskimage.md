---
title: Ivmvirtualpc-Methode "deatefloppydiskimage" ("vpccominterfaces. h")
description: Erstellt eine Disketten Image Datei.
ms.assetid: 474e86a4-2019-41bd-9361-e494291d1961
keywords:
- Methode "" der Methode "kreatefloppydiskimage"
- Methode "die Methode" für den virtuellen PC der Methode "" mit der Methode "ivmvirtualpc"
- Ivmvirtualpc Interface Virtual PC, Methode "kreatefloppydiskimage"
topic_type:
- apiref
api_name:
- IVMVirtualPC.CreateFloppyDiskImage
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ff94ba5cb922aeb75f4effac413bb83b080b3fd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478150"
---
# <a name="ivmvirtualpccreatefloppydiskimage-method"></a>Ivmvirtualpc:: kreatefloppydiskimage-Methode

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Erstellt eine Disketten Image Datei.

## <a name="syntax"></a>Syntax


```C++
HRESULT CreateFloppyDiskImage(
  [in] BSTR                  imagePath,
  [in] VMFloppyDiskImageType imageType
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ImagePath* \[ in\]
</dt> <dd>

Der vollständige Pfad zur neuen Datenträger Image Datei. Der enthaltende Ordner wird erstellt, wenn er nicht vorhanden ist.

</dd> <dt>

*ImageType* \[ in\]
</dt> <dd>

Der Typ des zu erstellenden Disketten Bilds. Nur **vmfloppydiskimage \_ lowdensity** (1) und **vmfloppydiskimage \_ highdensity** (2) werden unterstützt. Siehe [**vmfloppydiskimagetype**](vmfloppydiskimagetype.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode/-wert                                                                                                                                                                            | BESCHREIBUNG                                                                                                                                               |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                                                                                                         | Der Vorgang wurde durchgeführt.<br/>                                                                                                                  |
| <dl> <dt>**E \_ Zeiger**</dt> <dt>0x80004003</dt> </dl>                                    | Der *ImagePath* -Parameter ist **null**.<br/>                                                                                                         |
| <dl> <dt>**E \_ InvalidArg**</dt> <dt>0x80000003</dt> </dl>                                 | Der *ImageType* -Parameter ist nicht [**vmfloppydiskimage \_ lowdensity**](vmfloppydiskimagetype.md) (1) oder **vmfloppydiskimage \_ highdensity** (2).<br/> |
| <dl> <dt>**HRESULT \_ FROM \_ Win32 (Fehler \_ Pfad \_ nicht \_ gefunden)**</dt> <dt>0x80070003</dt> </dl> | Das System kann den durch den *ImagePath* -Parameter angegebenen Pfad nicht finden.<br/>                                                                        |
| <dl> <dt>**HRESULT \_ Von \_ Win32 ( \_ ungültiger \_ Name)**</dt> <dt>0x8007007b</dt> </dl>    | Der *ImagePath* -Parameter enthält ein ungültiges Zeichen (eines von " \* ?: <>/ \| " ").<br/>                                                           |
| <dl> <dt>**HRESULT \_ FROM \_ Win32 (Error ungültiger \_ \_ Pfadname)**</dt> <dt>0x800700a1</dt> </dl>    | Der *ImagePath* -Parameter gibt einen leeren oder relativen Pfad an. Ein absoluter Pfad ist erforderlich.<br/>                                                   |
| <dl> <dt>**HRESULT \_ Von \_ Win32 (Fehler \_ Puffer \_ Überlauf)**</dt> <dt>0x8007006f</dt> </dl> | Der durch den *ImagePath* -Parameter angegebene Pfad ist zu lang. Die Länge des Pfads muss weniger als 260 Zeichen umfassen.<br/>                          |
| <dl> <dt>**HRESULT \_ Von \_ Win32 (Fehler \_ bereits \_ vorhanden)**</dt> <dt>0x800700b7</dt> </dl>  | Die Datei, auf die der *ImagePath* -Parameter verweist, ist bereits vorhanden.<br/>                                                                               |
| <dl> <dt>**HRESULT \_ Von \_ Win32 (Fehler \_ \_**</dt> Datenträger voll) <dt>0x80070070</dt> </dl>       | Auf dem Host Volume ist nicht genügend Speicherplatz vorhanden, um das virtuelle Disketten Image zu erstellen.<br/>                                                        |
| <dl> <dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt> </dl>                            | Ein unerwarteter Fehler ist aufgetreten.<br/>                                                                                                                  |
| <dl> <dt>**VM \_ E \_ \_ Hardwarevirtualisierung \_ deaktiviert**</dt> <dt>0xa0040951</dt> </dl>     | Der Prozessor bietet keine Unterstützung für hav-Erweiterungen (Hardware Beschleunigung Virtualization).<br/>                                                           |



 

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

 

