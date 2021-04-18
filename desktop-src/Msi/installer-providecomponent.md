---
description: Die providecomponent-Methode des Installer-Objekts gibt den vollständigen Komponenten Pfad zurück und führt jede erforderliche Installation aus.
ms.assetid: 2bf09515-6f65-4712-89c1-01c43c1ce27c
title: Installer. providecomponent-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ProvideComponent
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e383c532d496ed217bdb7743b8171d732d61b2d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371159"
---
# <a name="installerprovidecomponent-method"></a>Installer. providecomponent-Methode

Die **providecomponent** -Methode des [**Installer**](installer-object.md) -Objekts gibt den vollständigen Komponenten Pfad zurück und führt jede erforderliche Installation aus. Bei Bedarf fordert die **providecomponent** -Methode des [**Installer**](installer-object.md) -Objekts zur Eingabe der Quelle auf und erhöht den Verwendungs Zähler für das Feature.

## <a name="syntax"></a>Syntax


```JScript
Installer.ProvideComponent(
  Product,
  Feature,
  Component,
  InstallMode
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

Gibt die Funktions-ID der Funktion an, die die Komponente enthält.

</dd> <dt>

*Komponente* 
</dt> <dd>

Gibt den Komponenten Code an.

</dd> <dt>

*InstallMode* 
</dt> <dd>

Definiert den Installationsmodus. Dieser Parameter kann einer der Werte sein, die in der folgenden Tabelle aufgeführt sind.



| Name                                                                                                                                                                                                                                                                                                                                                               | Bedeutung                                                                                                                                                                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiInstallModeDefault"></span><span id="msiinstallmodedefault"></span><span id="MSIINSTALLMODEDEFAULT"></span><dl> <dt>**msiinstallmodedefault**</dt> <dt>0</dt> </dl>                                                                                | Stellt den Komponenten Pfad bereit und führt ggf. eine beliebige Installation durch.<br/>                                                                                                                                                  |
| <span id="msiInstallModeExisting"></span><span id="msiinstallmodeexisting"></span><span id="MSIINSTALLMODEEXISTING"></span><dl> <dt>**msiinstallmodevorhandenes**</dt> <dt>– 1</dt> </dl>                                                                           | Gibt den Komponenten Pfad nur dann an, wenn das Feature vorhanden ist. Andernfalls wird eine leere Zeichenfolge zurückgegeben. Dieser Modus überprüft, ob die Schlüsseldatei der Komponente vorhanden ist.<br/>                                                                |
| <span id="msiInstallModeNoDetection"></span><span id="msiinstallmodenodetection"></span><span id="MSIINSTALLMODENODETECTION"></span><dl> <dt>**msiinstallmudenoerkennungs**</dt> <dt>– 2</dt> </dl>                                                               | Gibt den Komponenten Pfad nur dann an, wenn das Feature vorhanden ist. Andernfalls wird eine leere Zeichenfolge zurückgegeben. In diesem Modus wird die Registrierung der Komponente überprüft, aber es wird nicht überprüft, ob die Schlüsseldatei der Komponente vorhanden ist.<br/>                 |
| <span id="msiInstallModeNoSourceResolution"></span><span id="msiinstallmodenosourceresolution"></span><span id="MSIINSTALLMODENOSOURCERESOLUTION"></span><dl> <dt>**msiinstallmudenosourceresolution**</dt> <dt>– 3</dt> </dl>                                   | Stellt den Komponenten Pfad nur dann bereit, wenn die Funktion mit einem InstallState-Parameter von *msiinstallstatelocal* vorhanden ist. Dadurch wird die Registrierung der Komponente überprüft, aber es wird nicht überprüft, ob die Schlüsseldatei der Komponente vorhanden ist.<br/> |
| <span id="combination_of_the_msiReinstallMode_flags"></span><span id="combination_of_the_msireinstallmode_flags"></span><span id="COMBINATION_OF_THE_MSIREINSTALLMODE_FLAGS"></span><dl> <dt>**Kombination der msireinstallmode-Flags**</dt><dt></dt> </dl> | Ruft [**reinstallfeature**](installer-reinstallfeature.md) auf, um die Funktion mithilfe dieses Parameters für den *REINSTALLMODE* -Parameter erneut zu installieren, und stellt dann die Komponente bereit.<br/>                                           |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Die **providecomponent** -Methode kombiniert die Funktionalität von [**usefeature**](installer-usefeature.md), [**Konfigurierung**](installer-configurefeature.md)und [**componentpath**](installer-componentpath.md). Die **providecomponent** -Methode vereinfacht die Aufruf Sequenz, erhöht aber auch den Verwendungs Zähler und sollte mit Vorsicht verwendet werden, um eine ungenaue Verwendungs Anzahl zu verhindern. Die **providecomponent** -Methode bietet auch weniger Flexibilität als eine Reihe einzelner Aufrufe der bereits erwähnten Methoden und Eigenschaften.

Wenn die Anwendung nach einer unerwarteten Situation wieder hergestellt wird, hat die Anwendung wahrscheinlich bereits [**usefeature**](installer-usefeature.md) aufgerufen und die Verwendungs Anzahl erhöht. In diesem Fall sollte die Anwendung das Erhöhen der Verwendungs Anzahl vermeiden, indem anstelle der **providecomponent** -Methode die Methode " [**Konfigurierung**](installer-configurefeature.md) " aufgerufen wird.

Die msiinstallmodevorhandene-Option kann nicht in Kombination mit msireinstallmode-Flags verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ iinstaller ist definiert als 000c1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MsiProvideComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidecomponenta)
</dt> </dl>

 

 




