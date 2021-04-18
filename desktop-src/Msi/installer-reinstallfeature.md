---
description: Die reinstallfeature-Methode des Installer-Objekts installiert Features neu oder korrigiert Probleme mit den installierten Funktionen.
ms.assetid: cfe2aef4-7742-49cd-b7a3-7d484e1f85e3
title: Installer. reinstallfeature-Methode
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
ms.openlocfilehash: a6bac008ee7121bbcb985b9a8ff5ba02df122266
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371298"
---
# <a name="installerreinstallfeature-method"></a>Installer. reinstallfeature-Methode

Die **reinstallfeature** -Methode des [**Installer**](installer-object.md) -Objekts installiert Features neu oder korrigiert Probleme mit den installierten Funktionen.

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

Gibt das neu zu installierende Feature an. Das übergeordnete Feature oder die untergeordnete Funktion der angegebenen Funktion wird nicht neu installiert. Um das übergeordnete oder untergeordnete Feature erneut zu installieren, müssen Sie die **reinstallfeature** -Methode für jeden separaten Befehl oder die [**reinstallproduct**](installer-reinstallproduct.md) -Methode verwenden.

</dd> <dt>

*Rein Stall Mode* 
</dt> <dd>

Gibt den Typ der erneuten Installation an. Dieser Parameter kann einen oder mehrere der folgenden Werte aufweisen.



| Wert                                                                                                                                                                                                                                                                    | Bedeutung                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <span id="msiReinstallModeFileMissing"></span><span id="msireinstallmodefilemissing"></span><span id="MSIREINSTALLMODEFILEMISSING"></span><dl> <dt>**msireinstallmudefilemissing**</dt> </dl>                     | Wird nur neu installiert, wenn die Datei fehlt.<br/>                                |
| <span id="msiReinstallModeFileOlderVersion"></span><span id="msireinstallmodefileolderversion"></span><span id="MSIREINSTALLMODEFILEOLDERVERSION"></span><dl> <dt>**msireinstallmudefileolderversion**</dt> </dl> | Wird neu installiert, wenn die Datei fehlt oder eine ältere Version ist.<br/>              |
| <span id="msiReinstallModeFileEqualVersion"></span><span id="msireinstallmodefileequalversion"></span><span id="MSIREINSTALLMODEFILEEQUALVERSION"></span><dl> <dt>**msireinstallmudefileequalversion**</dt> </dl> | Wird neu installiert, wenn die Datei fehlt oder eine gleichmäßige oder eine ältere Version ist.<br/>     |
| <span id="msiReinstallModeFileExact"></span><span id="msireinstallmodefileexact"></span><span id="MSIREINSTALLMODEFILEEXACT"></span><dl> <dt>**msireinstallmudefileexact**</dt> </dl>                             | Wird neu installiert, wenn die Datei fehlt oder eine exakte Version ist.<br/>          |
| <span id="msiReinstallModeFileVerify"></span><span id="msireinstallmodefileverify"></span><span id="MSIREINSTALLMODEFILEVERIFY"></span><dl> <dt>**msireinstallmudefileverify**</dt> </dl>                         | Prüft die Summe der ausführbaren Dateien und installiert sie neu, wenn Sie nicht vorhanden oder beschädigt sind.<br/> |
| <span id="msiReinstallModeFileReplace"></span><span id="msireinstallmodefilereplace"></span><span id="MSIREINSTALLMODEFILEREPLACE"></span><dl> <dt>**msireinstallmodefilereplace**</dt> </dl>                     | Installiert alle Dateien unabhängig von der Version neu.<br/>                            |
| <span id="msiReinstallModeUserData"></span><span id="msireinstallmodeuserdata"></span><span id="MSIREINSTALLMODEUSERDATA"></span><dl> <dt>**msireinstallmudeuserdata**</dt> </dl>                                 | Stellt sicher, dass pro = Benutzer Registrierungseinträge erforderlich ist.<br/>                            |
| <span id="msiReinstallModeMachineData"></span><span id="msireinstallmodemachinedata"></span><span id="MSIREINSTALLMODEMACHINEDATA"></span><dl> <dt>**msireinstallmodemachinedata**</dt> </dl>                     | Stellt die erforderlichen Anforderungen pro = Computer Registrierungseinträge sicher.<br/>                         |
| <span id="msiReinstallModeShortcut"></span><span id="msireinstallmodeshortcut"></span><span id="MSIREINSTALLMODESHORTCUT"></span><dl> <dt>**msireinstallmodeshortcut**</dt> </dl>                                 | Überprüft Verknüpfungen.<br/>                                                   |
| <span id="msiReinstallModePackage"></span><span id="msireinstallmodepackage"></span><span id="MSIREINSTALLMODEPACKAGE"></span><dl> <dt>**"msireinstallmodepackage"**</dt> </dl>                                     | Verwendet die Recache-Quelle, um das Paket zu installieren.<br/>                        |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ iinstaller ist definiert als 000c1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Msireinstallfeature**](/windows/desktop/api/Msi/nf-msi-msireinstallfeaturea)
</dt> <dt>

[Installations-und Konfigurationsfunktionen](installer-function-reference.md)
</dt> </dl>

 

 




