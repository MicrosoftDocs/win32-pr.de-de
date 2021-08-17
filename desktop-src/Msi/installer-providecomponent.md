---
description: Die ProvideComponent-Methode des Installer-Objekts gibt den vollständigen Komponentenpfad zurück und führt alle erforderlichen Installationen aus.
ms.assetid: 2bf09515-6f65-4712-89c1-01c43c1ce27c
title: Installer.ProvideComponent-Methode
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
ms.openlocfilehash: 49e3808fdad44e4bc3cb7312c1b352874eab3b768920f23ac198811d29f6c8ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118630328"
---
# <a name="installerprovidecomponent-method"></a>Installer.ProvideComponent-Methode

Die **ProvideComponent-Methode** des [**Installer-Objekts**](installer-object.md) gibt den vollständigen Komponentenpfad zurück und führt alle erforderlichen Installationen aus. Bei Bedarf fordert die **ProvideComponent-Methode** des [**Installer-Objekts**](installer-object.md) zur Eingabe der Quelle auf und erhöht die Nutzungsanzahl für das Feature.

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

Gibt die Feature-ID des Features an, das die Komponente enthält.

</dd> <dt>

*Komponente* 
</dt> <dd>

Gibt den Komponentencode an.

</dd> <dt>

*InstallMode* 
</dt> <dd>

Definiert den Installationsmodus. Dieser Parameter kann einer der in der folgenden Tabelle gezeigten Werte sein.



| Name                                                                                                                                                                                                                                                                                                                                                               | Bedeutung                                                                                                                                                                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiInstallModeDefault"></span><span id="msiinstallmodedefault"></span><span id="MSIINSTALLMODEDEFAULT"></span><dl> <dt>**msiInstallModeDefault**</dt> <dt>0</dt> </dl>                                                                                | Stellt den Komponentenpfad zur Durchführung einer Installation bei Bedarf zur<br/>                                                                                                                                                  |
| <span id="msiInstallModeExisting"></span><span id="msiinstallmodeexisting"></span><span id="MSIINSTALLMODEEXISTING"></span><dl> <dt>**msiInstallModeExisting**</dt> <dt>–1</dt> </dl>                                                                           | Stellt den Komponentenpfad nur bei vorhandener Funktion zur andernfalls gibt eine leere Zeichenfolge zurück. Dieser Modus überprüft das Vorhandensein der Schlüsseldatei der Komponente.<br/>                                                                |
| <span id="msiInstallModeNoDetection"></span><span id="msiinstallmodenodetection"></span><span id="MSIINSTALLMODENODETECTION"></span><dl> <dt>**msiInstallModeNoDetection**</dt> <dt>–2</dt> </dl>                                                               | Stellt den Komponentenpfad nur dann zur Unterstützung bei, wenn das Feature vorhanden ist. Andernfalls gibt eine leere Zeichenfolge zurück. Dieser Modus überprüft die Registrierung der Komponente, überprüft jedoch nicht das Vorhandensein der Schlüsseldatei der Komponente.<br/>                 |
| <span id="msiInstallModeNoSourceResolution"></span><span id="msiinstallmodenosourceresolution"></span><span id="MSIINSTALLMODENOSOURCERESOLUTION"></span><dl> <dt>**msiInstallModeNoSourceResolution**</dt> <dt>–3</dt> </dl>                                   | Stellt den Komponentenpfad nur dann zur Verfügung, wenn das Feature mit dem InstallState-Parameter *msiInstallStateLocal vorhanden ist.* Dadurch wird die Registrierung der Komponente überprüft, aber nicht das Vorhandensein der Schlüsseldatei der Komponente.<br/> |
| <span id="combination_of_the_msiReinstallMode_flags"></span><span id="combination_of_the_msireinstallmode_flags"></span><span id="COMBINATION_OF_THE_MSIREINSTALLMODE_FLAGS"></span><dl> <dt>**Kombination der msiReinstallMode-Flags**</dt><dt></dt> </dl> | Ruft [**ReinstallFeature auf,**](installer-reinstallfeature.md) um das Feature mit diesem Parameter für den *ReinstallMode-Parameter* neu zu installieren, und stellt dann die Komponente zur Anwendung.<br/>                                           |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Die **ProvideComponent-Methode** kombiniert die Funktionen von [**UseFeature,**](installer-usefeature.md) [**ConfigureFeature**](installer-configurefeature.md)und [**ComponentPath.**](installer-componentpath.md) Die **ProvideComponent-Methode** vereinfacht die aufrufende Sequenz, erhöht jedoch auch die Nutzungsanzahl und sollte mit Vorsicht verwendet werden, um ungenaue Nutzungsanzahlen zu verhindern. Die **ProvideComponent-Methode** bietet auch weniger Flexibilität als eine Reihe einzelner Aufrufe der zuvor erwähnten Methoden und Eigenschaften.

Wenn die Anwendung nach einer unerwarteten Situation wiederhergestellt wird, hat die Anwendung wahrscheinlich bereits [**UseFeature**](installer-usefeature.md) aufgerufen und die Nutzungsanzahl erhöht. In diesem Fall sollte die Anwendung vermeiden, die Nutzungsanzahl durch Aufrufen der [**ConfigureFeature-Methode**](installer-configurefeature.md) anstelle der **ProvideComponent-Methode zu** erhöhen.

Die Option msiInstallModeExisting kann nicht in Kombination mit msiReinstallMode-Flags verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller ist als 000C1090-0000-0000-C000-00000000046 definiert.<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**MsiProvideComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidecomponenta)
</dt> </dl>

 

 




