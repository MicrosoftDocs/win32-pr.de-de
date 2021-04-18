---
description: Die providequalifiedcomponent-Methode des Installer-Objekts gibt den vollständigen Komponenten Pfad zurück und führt jede erforderliche Installation aus. Bei Bedarf fordert diese Methode zur Eingabe der Quelle auf und erhöht den Verwendungs Zähler für das Feature.
ms.assetid: 4f9a5094-1556-4d86-8b51-c8c3ce1cbed4
title: Installer. providequalifiedcomponent-Methode
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
ms.openlocfilehash: 73c830610b49976e3625dd333c57f39e43d4be14
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357721"
---
# <a name="installerprovidequalifiedcomponent-method"></a>Installer. providequalifiedcomponent-Methode

Die **providequalifiedcomponent** -Methode des [**Installer**](installer-object.md) -Objekts gibt den vollständigen Komponenten Pfad zurück und führt jede erforderliche Installation aus. Bei Bedarf fordert diese Methode zur Eingabe der Quelle auf und erhöht den Verwendungs Zähler für das Feature.

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

Gibt die Komponenten-ID für die angeforderte Komponente an. Dies ist möglicherweise nicht die GUID für die Komponente selbst, sondern ein Server, der die richtige Funktionalität bereitstellt, wie in der Spalte ComponentID der [Tabelle PublishComponent](publishcomponent-table.md).

</dd> <dt>

*Qualifizierer* 
</dt> <dd>

Gibt einen Qualifizierer in einer Liste von werbekomponenten an (aus der [PublishComponent-Tabelle](publishcomponent-table.md)).

</dd> <dt>

*InstallMode* 
</dt> <dd>

Definiert den Installationsmodus. Dieser Parameter kann einer der Werte sein, die in der folgenden Tabelle aufgeführt sind.



| InstallMode                                                                                                                                                                                                                                                                                                                                                         | Bedeutung                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiInstallModeDefault"></span><span id="msiinstallmodedefault"></span><span id="MSIINSTALLMODEDEFAULT"></span><dl> <dt>**msiinstallmodedefault**</dt> <dt>0</dt> </dl>                                                                                 | Stellt die-Komponente bereit und führt jede erforderliche Installation aus.<br/>                                                                                                                                                           |
| <span id="msiInstallModeExisting"></span><span id="msiinstallmodeexisting"></span><span id="MSIINSTALLMODEEXISTING"></span><dl> <dt>**msiinstallmodevorhandenes**</dt> <dt>– 1</dt> </dl>                                                                            | Stellt die Komponente nur bereit, wenn das Feature vorhanden ist. Andernfalls wird eine leere Zeichenfolge zurückgegeben. Dieser Modus überprüft, ob die Schlüsseldatei der Komponente vorhanden ist.<br/>                                                                      |
| <span id="msiInstallModeNoDetection"></span><span id="msiinstallmodenodetection"></span><span id="MSIINSTALLMODENODETECTION"></span><dl> <dt>**msiinstallmudenoerkennungs**</dt> <dt>– 2</dt> </dl>                                                                | Stellt die Komponente nur bereit, wenn das Feature vorhanden ist. Andernfalls wird eine leere Zeichenfolge zurückgegeben. In diesem Modus wird nur überprüft, ob die Komponente registriert ist, aber es wird nicht überprüft, ob die Schlüsseldatei der Komponente vorhanden ist.<br/>              |
| <span id="msiInstallModeNoSourceResolution"></span><span id="msiinstallmodenosourceresolution"></span><span id="MSIINSTALLMODENOSOURCERESOLUTION"></span><dl> <dt>**msiinstallmudenosourceresolution**</dt> <dt>– 3</dt> </dl>                                    | Stellt den Komponenten Pfad nur dann bereit, wenn die Funktion mit einem InstallState-Parameter von *msiinstallstatelocal* vorhanden ist. Dadurch wird die Registrierung der Komponente überprüft, aber es wird nicht überprüft, ob die Schlüsseldatei der Komponente vorhanden ist.<br/> |
| <span id="combination_of_the_msiReinstallMode_flags"></span><span id="combination_of_the_msireinstallmode_flags"></span><span id="COMBINATION_OF_THE_MSIREINSTALLMODE_FLAGS"></span><dl> <dt>**Kombination der msireinstallmode-Flags**</dt> <dt></dt> </dl> | Ruft [**reinstallfeature**](installer-reinstallfeature.md) auf, um die Funktion mithilfe dieses Parameters für den *REINSTALLMODE* -Parameter erneut zu installieren, und stellt dann die Komponente bereit.<br/>                                           |



 

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

[**Msiprovidequalifiedcomponent**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponenta)
</dt> </dl>

 

 




