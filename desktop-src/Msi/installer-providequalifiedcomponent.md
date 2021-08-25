---
description: Die ProvideQualifiedComponent-Methode des Installer-Objekts gibt den vollständigen Komponentenpfad zurück und führt alle erforderlichen Installationen aus. Bei Bedarf fordert diese Methode zur Eingabe der Quelle auf und erhöht die Nutzungsanzahl für das Feature.
ms.assetid: 4f9a5094-1556-4d86-8b51-c8c3ce1cbed4
title: Installer.ProvideQualifiedComponent-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ProvideQualifiedComponent
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 534f0d29fed41a495c3432ff757d7e269c6b2a5d63c9bfabebe614849f3ab9f6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119828870"
---
# <a name="installerprovidequalifiedcomponent-method"></a>Installer.ProvideQualifiedComponent-Methode

Die **ProvideQualifiedComponent-Methode** des [**Installer-Objekts**](installer-object.md) gibt den vollständigen Komponentenpfad zurück und führt alle erforderlichen Installationen aus. Bei Bedarf fordert diese Methode zur Eingabe der Quelle auf und erhöht die Nutzungsanzahl für das Feature.

## <a name="syntax"></a>Syntax


```JScript
Installer.ProvideQualifiedComponent(
  Category,
  Qualifier,
  InstallMode
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Kategorie* 
</dt> <dd>

Gibt die Komponenten-ID für die angeforderte Komponente an. Dies ist möglicherweise nicht die GUID für die Komponente selbst, sondern ein Server, der die richtige Funktionalität bereitstellt, wie in der ComponentId -Spalte der [PublishComponent-Tabelle](publishcomponent-table.md).

</dd> <dt>

*Qualifizierer* 
</dt> <dd>

Gibt einen Qualifizierer in eine Liste von Werbekomponenten (aus [der PublishComponent-Tabelle)](publishcomponent-table.md)an.

</dd> <dt>

*InstallMode* 
</dt> <dd>

Definiert den Installationsmodus. Dieser Parameter kann einer der in der folgenden Tabelle aufgeführten Werte sein.



| InstallMode                                                                                                                                                                                                                                                                                                                                                         | Bedeutung                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiInstallModeDefault"></span><span id="msiinstallmodedefault"></span><span id="MSIINSTALLMODEDEFAULT"></span><dl> <dt>**msiInstallModeDefault**</dt> <dt>0</dt> </dl>                                                                                 | Stellt die Komponente bereit und führt alle erforderlichen Installationen durch.<br/>                                                                                                                                                           |
| <span id="msiInstallModeExisting"></span><span id="msiinstallmodeexisting"></span><span id="MSIINSTALLMODEEXISTING"></span><dl> <dt>**msiInstallModeExisting**</dt> <dt>–1</dt> </dl>                                                                            | Stellt die Komponente nur bereit, wenn das Feature vorhanden ist. andernfalls wird eine leere Zeichenfolge zurückgegeben. In diesem Modus wird überprüft, ob die Schlüsseldatei der Komponente vorhanden ist.<br/>                                                                      |
| <span id="msiInstallModeNoDetection"></span><span id="msiinstallmodenodetection"></span><span id="MSIINSTALLMODENODETECTION"></span><dl> <dt>**msiInstallModeNoDetection**</dt> <dt>–2</dt> </dl>                                                                | Stellt die Komponente nur bereit, wenn das Feature vorhanden ist. andernfalls wird eine leere Zeichenfolge zurückgegeben. In diesem Modus wird nur überprüft, ob die Komponente registriert ist, aber nicht das Vorhandensein der Schlüsseldatei der Komponente.<br/>              |
| <span id="msiInstallModeNoSourceResolution"></span><span id="msiinstallmodenosourceresolution"></span><span id="MSIINSTALLMODENOSOURCERESOLUTION"></span><dl> <dt>**msiInstallModeNoSourceResolution**</dt> <dt>–3</dt> </dl>                                    | Stellt den Komponentenpfad nur bereit, wenn das Feature mit dem InstallState-Parameter *msiInstallStateLocal* vorhanden ist. Dadurch wird die Registrierung der Komponente überprüft, aber nicht das Vorhandensein der Schlüsseldatei der Komponente.<br/> |
| <span id="combination_of_the_msiReinstallMode_flags"></span><span id="combination_of_the_msireinstallmode_flags"></span><span id="COMBINATION_OF_THE_MSIREINSTALLMODE_FLAGS"></span><dl> <dt>**Kombination der msiReinstallMode-Flags**</dt> <dt></dt> </dl> | Ruft [**ReinstallFeature**](installer-reinstallfeature.md) auf, um das Feature mit diesem Parameter für den *ReinstallMode-Parameter* neu zu installieren, und stellt dann die Komponente bereit.<br/>                                           |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installationsprogramm 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller ist als 000C1090-0000-0000-C000-0000000000046 definiert.<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MsiProvideQualifiedComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponenta)
</dt> </dl>

 

 




