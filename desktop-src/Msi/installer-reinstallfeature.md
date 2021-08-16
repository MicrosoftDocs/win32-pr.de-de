---
description: Mit der ReinstallFeature-Methode des Installer-Objekts werden Features neu installiert oder Probleme mit installierten Features korrigiert.
ms.assetid: cfe2aef4-7742-49cd-b7a3-7d484e1f85e3
title: Installer.ReinstallFeature-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ReinstallFeature
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: dfe4cb96ccac85fb5b94f3a2a8ec3dcca48f6fa4300a6bceb338b2ebbe01da22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118946286"
---
# <a name="installerreinstallfeature-method"></a>Installer.ReinstallFeature-Methode

Mit **der ReinstallFeature-Methode** des [**Installer-Objekts**](installer-object.md) werden Features neu installiert oder Probleme mit installierten Features korrigiert.

## <a name="syntax"></a>Syntax


```JScript
Installer.ReinstallFeature(
  Product,
  Feature,
  ReinstallMode
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Produkt* 
</dt> <dd>

Gibt den Produktcode des Produkts an.

</dd> <dt>

*Feature* 
</dt> <dd>

Gibt das neu zu installierende Feature an. Das übergeordnete Feature oder untergeordnete Feature des angegebenen Features wird nicht neu installiert. Um das übergeordnete oder untergeordnete Feature neu zu installieren, müssen Sie die **ReinstallFeature-Methode** für jedes feature separat aufrufen oder die [**ReinstallProduct-Methode**](installer-reinstallproduct.md) verwenden.

</dd> <dt>

*Reinstallmode* 
</dt> <dd>

Gibt den Typ der Neuinstallation an. Dieser Parameter kann einen oder mehrere der folgenden Werte sein.



| Wert                                                                                                                                                                                                                                                                    | Bedeutung                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <span id="msiReinstallModeFileMissing"></span><span id="msireinstallmodefilemissing"></span><span id="MSIREINSTALLMODEFILEMISSING"></span><dl> <dt>**msiReinstallModeFileMissing**</dt> </dl>                     | Wird nur dann neu installiert, wenn die Datei fehlt.<br/>                                |
| <span id="msiReinstallModeFileOlderVersion"></span><span id="msireinstallmodefileolderversion"></span><span id="MSIREINSTALLMODEFILEOLDERVERSION"></span><dl> <dt>**msiReinstallModeFileOlderVersion**</dt> </dl> | Wird neu installiert, wenn die Datei fehlt oder eine ältere Version ist.<br/>              |
| <span id="msiReinstallModeFileEqualVersion"></span><span id="msireinstallmodefileequalversion"></span><span id="MSIREINSTALLMODEFILEEQUALVERSION"></span><dl> <dt>**msiReinstallModeFileEqualVersion**</dt> </dl> | Wird neu installiert, wenn die Datei fehlt oder eine gleich oder ältere Version ist.<br/>     |
| <span id="msiReinstallModeFileExact"></span><span id="msireinstallmodefileexact"></span><span id="MSIREINSTALLMODEFILEEXACT"></span><dl> <dt>**msiReinstallModeFileExact**</dt> </dl>                             | Wird neu installiert, wenn die Datei fehlt oder keine exakte Version ist.<br/>          |
| <span id="msiReinstallModeFileVerify"></span><span id="msireinstallmodefileverify"></span><span id="MSIREINSTALLMODEFILEVERIFY"></span><dl> <dt>**msiReinstallModeFileVerify**</dt> </dl>                         | Überprüft die Summe ausführbarer Dateien und installiert sie neu, wenn sie fehlen oder beschädigt sind.<br/> |
| <span id="msiReinstallModeFileReplace"></span><span id="msireinstallmodefilereplace"></span><span id="MSIREINSTALLMODEFILEREPLACE"></span><dl> <dt>**msiReinstallModeFileReplace**</dt> </dl>                     | Installiert alle Dateien unabhängig von der Version neu.<br/>                            |
| <span id="msiReinstallModeUserData"></span><span id="msireinstallmodeuserdata"></span><span id="MSIREINSTALLMODEUSERDATA"></span><dl> <dt>**msiReinstallModeUserData**</dt> </dl>                                 | Stellt die erforderlichen Registrierungseinträge pro Benutzer sicher.<br/>                            |
| <span id="msiReinstallModeMachineData"></span><span id="msireinstallmodemachinedata"></span><span id="MSIREINSTALLMODEMACHINEDATA"></span><dl> <dt>**msiReinstallModeMachineData**</dt> </dl>                     | Stellt die erforderlichen Registrierungseinträge pro Computer sicher.<br/>                         |
| <span id="msiReinstallModeShortcut"></span><span id="msireinstallmodeshortcut"></span><span id="MSIREINSTALLMODESHORTCUT"></span><dl> <dt>**msiReinstallModeShortcut**</dt> </dl>                                 | Überprüft Verknüpfungen.<br/>                                                   |
| <span id="msiReinstallModePackage"></span><span id="msireinstallmodepackage"></span><span id="MSIREINSTALLMODEPACKAGE"></span><dl> <dt>**msiReinstallModePackage**</dt> </dl>                                     | Verwendet die Recachequelle, um das Paket zu installieren.<br/>                        |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller ist als 000C1090-0000-0000-C000-00000000046 definiert.<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**MsiReinstallFeature**](/windows/desktop/api/Msi/nf-msi-msireinstallfeaturea)
</dt> <dt>

[Installations- und Konfigurationsfunktionen](installer-function-reference.md)
</dt> </dl>

 

 




