---
title: Registrierungsflags
description: Registrierungsflags
ms.assetid: ba1709c2-0fe5-4168-9aed-613d01eff21f
keywords:
- Windows Media Player-Plug-Ins,Registrierungsflags
- Plug-Ins, Registrierungsflags
- Benutzeroberflächen-Plug-Ins, Registrierungsflags
- Benutzeroberflächen-Plug-Ins, Registrierungsflags
- Flags, Benutzeroberflächen-Plug-Ins
- Registrierung, Benutzeroberflächen-Plug-Ins
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afbd34ed98236f8a02c936d52b092b82be60b986fb7b16edce1f3b1cbb91d6a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120002810"
---
# <a name="registration-flags"></a>Registrierungsflags

Wenn der Windows Media Player-Plug-In-Assistent ein neues Benutzeroberflächen-Plug-In-Projekt erstellt, wird ein Schlüssel in der Registrierung erstellt, der Informationen zum Plug-In enthält. Dieser Schlüssel wird an folgendem Speicherort erstellt:


```C++
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MediaPlayer\UIPlugins\{ClassId}
```



*ClassId* ist die Klassen-ID des Plug-Ins.

Dieser Schlüssel enthält die folgenden Werte.



| Name                     | type       | BESCHREIBUNG                                                                                                                                                                               |
|--------------------------|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Funktionen             | REG \_ DWORD | Ein DWORD-Wert, der aus mindestens einem Plug-In-Typflag besteht, das mithilfe binärer OR-Vorgänge mit einem oder mehreren Plug-In-Funktionenflags kombiniert werden kann.                             |
| BESCHREIBUNG              | REG \_ SZ    | Eine Zeichenfolge, die die Beschreibung des Plug-Ins enthält. Der Plug-In-Assistent erstellt eine Zeichenfolgenressource und stellt die URL der Ressource (mithilfe des res-Protokolls) für diesen Wert zur Seite.         |
| FriendlyName             | REG \_ SZ    | Eine Zeichenfolge, die den für den Benutzer lesbaren Namen für das Plug-In enthält. Der Plug-In-Assistent erstellt eine Zeichenfolgenressource und stellt die URL der Ressource (mithilfe des res-Protokolls) für diesen Wert zur Seite. |
| UninstallPath (optional) | REG \_ SZ    | Eine Zeichenfolge, die den Pfad zu einer ausführbaren Datei enthält, die das Plug-In deinstalliert.                                                                                                        |



 

Weitere Informationen zum Res-Protokoll finden Sie im Internet Development SDK.

In der folgenden Tabelle werden die Plug-In-Typflags aufgeführt.



| Plug-In-Typflag                | Wert | BESCHREIBUNG                                       |
|----------------------------------|-------|---------------------------------------------------|
| **HINTERGRUND DES \_ PLUG-IN-TYPS \_**     | 0x1   | Das Benutzeroberflächen-Plug-In zeigt keine Benutzeroberfläche an. |
| **\_ \_ PLUG-IN-TYP SEPARATEWINDOW** | 0x2   | Das Benutzeroberflächen-Plug-In ist ein separates Fenster-Plug-In.      |
| **\_ \_ PLUG-IN-TYP DISPLAYAREA**    | 0x3   | Das Benutzeroberflächen-Plug-In ist ein Anzeigebereichs-Plug-In.         |
| **\_ \_ PLUG-IN-TYPEINSTELLUNGENBEREICH**   | 0x4   | Das Benutzeroberflächen-Plug-In ist ein Einstellungsbereichs-Plug-In.        |
| **\_ \_ PLUG-IN-TYP METADATAAREA**   | 0x5   | Das Benutzeroberflächen-Plug-In ist ein Metadatenbereich-Plug-In.        |



 

In der folgenden Tabelle werden die Plug-In-Funktionenflags aufgeführt.



| Flag für Plug-In-Funktionen             | Wert      | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                         |
|---------------------------------------|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_PLUG-IN-FLAGS \_ ACCEPTSMEDIA**       | 0x10000000 | Das Benutzeroberflächen-Plug-In kann Medienobjektzeigerarrays akzeptieren, wenn Windows Media Player [**IWMPPluginUI::SetProperty aufruft.**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-setproperty)                                                                                                                                                                                                                                                            |
| **\_PLUG-IN-FLAGS \_ AKZEPTIERENPLAYLISTS**   | 0x8000000  | Das Benutzeroberflächen-Plug-In kann Playlist-Objektzeigerarrays akzeptieren, wenn Windows Media Player [**IWMPPluginUI::SetProperty aufruft.**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-setproperty)                                                                                                                                                                                                                                                         |
| **\_PLUG-IN-FLAGS \_ HASPRESETS**         | 0x4000000  | Das Benutzeroberflächen-Plug-In verwendet Voreinstellungen. Wenn das Plug-In dieses Flag angibt, Windows Media Player das Plug-In auf voreingestellte Informationen durch Aufrufen [**von IWMPPluginUI::GetProperty abfragen.**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-getproperty)                                                                                                                                                                                                      |
| **\_PLUG-IN-FLAGS \_ HASPROPERTYPAGE**    | 0x80000000 | Das Benutzeroberflächen-Plug-In stellt ein Eigenschaftenseitendialogfeld zur Verfügung. Windows Media Player ruft [**IWMPPluginUI::D isplayPropertyPage**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-displaypropertypage) auf, wenn dieses Flag festgelegt wird, wenn die Eigenschaftenseite aufgerufen wird.                                                                                                                                                                                                 |
| **\_PLUG-IN-FLAGS \_ AUSGEBLENDET**             | 0x02000000 | Das Benutzeroberflächen-Plug-In für den Hintergrund wird nicht im  **Plug-In-Menü**  angezeigt, auf das über die Menüs Ansicht oder **Extras** oder über die Schaltfläche Jetzt abspielte Optionen auswählen in Jetzt abspielt zugegriffen wird. Er wird auf der **Registerkarte Plug-Ins des Dialogfelds** Optionen angezeigt. Dies führt dazu, dass das Symbol Ausgeführtes Hintergrund-Plug-In in der Statusleiste angezeigt wird. Dieses Flag hat keine Auswirkungen auf Plug-Ins, die keine Hintergrund-UI-Plug-Ins sind.<br/> |
| **\_PLUG-IN-FLAGS \_ INSTALLAUTORUN**     | 0x40000000 | Windows Media Player das Benutzeroberflächen-Plug-In automatisch ausgeführt, wenn das Plug-In installiert wird.                                                                                                                                                                                                                                                                                                                               |
| **\_PLUG-IN-FLAGS \_ LAUNCHPROPERTYPAGE** | 0x20000000 | Windows Media Player [**aufruft IWMPPluginUI::D isplayPropertyPage,**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-displaypropertypage) wenn das Benutzeroberflächen-Plug-In zum ersten Mal ausgeführt wird. Wenn dieses Flag angegeben wird, **sollte AUCH \_ PLUG-IN-FLAGS \_ HASPROPERTYPAGE** angegeben werden.<br/>                                                                                                                                                             |



 

Die folgenden Konstanten sind in wmpplug.h definiert. Ändern Sie nicht die Werte, die diesen Konstanten zugeordnet sind.



| Name                                    | BESCHREIBUNG                               |
|-----------------------------------------|-------------------------------------------|
| **\_PLUG-IN INSTALLREGKEY**               | Der Speicherort des Plug-In-Registrierungsschlüssels. |
| **PLUGIN \_ INSTALLREGKEY \_ FRIENDLYNAME** | Der Name des Werts für den Benutzerfreundlichen Namen.      |
| **PLUGIN \_ INSTALLREGKEY \_ DESCRIPTION**  | Der Name des Beschreibungswerts.        |
| **\_PLUG-IN-INSTALLATIONREGKEY-FUNKTIONEN \_** | Der Name des Werts der Funktionen.       |
| **\_PLUG-IN: \_ INSTALLREGKEY-DEINSTALLATION**    | Der Name des Deinstallationspfadwerts.     |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IWMPPluginUI::D isplayPropertyPage**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-displaypropertypage)
</dt> <dt>

[**IWMPPluginUI::GetProperty**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-getproperty)
</dt> <dt>

[**IWMPPluginUI::SetProperty**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-setproperty)
</dt> <dt>

[**Benutzeroberfläche Plug-Ins – Programmierreferenz**](user-interface-plug-ins-programming-reference.md)
</dt> </dl>

 

 





