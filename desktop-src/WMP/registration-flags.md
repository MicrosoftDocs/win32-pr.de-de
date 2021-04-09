---
title: Registrierungsflags
description: Registrierungsflags
ms.assetid: ba1709c2-0fe5-4168-9aed-613d01eff21f
keywords:
- Windows Media Player-Plug-ins, Registrierungsflags
- Plug-ins, Registrierungsflags
- Benutzerschnittstellen-Plug-ins, Registrierungsflags
- UI-Plug-ins, Registrierungsflags
- Flags, Benutzerschnittstellen-Plug-ins
- Registrierung, UI-Plug-ins
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac609b45866cd5f18edf61dffc2d3b7ac3c397ac
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104038567"
---
# <a name="registration-flags"></a>Registrierungsflags

Wenn der Assistent für den Windows Media Player-Plug-in ein neues Plug-in-Projekt für die Benutzeroberfläche erstellt, erstellt er einen Schlüssel in der Registrierung, der Informationen zum Plug-in enthält. Dieser Schlüssel wird am folgenden Speicherort erstellt:


```C++
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MediaPlayer\UIPlugins\{ClassId}
```



*ClassID* ist die Klassen-ID des Plug-ins.

Dieser Schlüssel umfasst die folgenden Werte:



| Name                     | type       | BESCHREIBUNG                                                                                                                                                                               |
|--------------------------|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Funktionen             | REG \_ DWORD | Ein DWORD-Wert, der aus mindestens einem Plug-in-Typflag besteht, das mit einem oder mehreren Plug-in-Funktionen-Flags mithilfe von binären-oder-Vorgängen kombiniert werden kann.                             |
| BESCHREIBUNG              | REG- \_ SZ    | Eine Zeichenfolge, die die Beschreibung des Plug-Ins enthält. Der Plug-in-Assistent erstellt eine Zeichen folgen Ressource und stellt die URL der Ressource (mit dem res-Protokoll) für diesen Wert bereit.         |
| FriendlyName             | REG- \_ SZ    | Eine Zeichenfolge, die den vom Benutzer lesbaren Namen für das Plug-in enthält. Der Plug-in-Assistent erstellt eine Zeichen folgen Ressource und stellt die URL der Ressource (mit dem res-Protokoll) für diesen Wert bereit. |
| Uninstallpath (optional) | REG- \_ SZ    | Eine Zeichenfolge, die den Pfad zu einer ausführbaren Datei enthält, die das Plug-in deinstalliert.                                                                                                        |



 

Weitere Informationen zum res-Protokoll finden Sie unter Internet Development SDK.

In der folgenden Tabelle werden die Plug-in-typanflags ausführlich erläutert.



| Plug-in-Typ-Flag                | Wert | BESCHREIBUNG                                       |
|----------------------------------|-------|---------------------------------------------------|
| **Hintergrund des Plug-Ins \_ \_**     | 0x1   | Im UI-Plug-in wird keine Benutzeroberfläche angezeigt. |
| **Plug-in- \_ Typ \_ trennfenster** | 0x2   | Das UI-Plug-in ist ein separates Fenster-Plug-in.      |
| **Anzeigebereich des Plug-Ins \_ \_**    | 0x3   | Das UI-Plug-in ist ein Anzeige Bereichs-Plug-in.         |
| **Einstellungsart des Plug-Ins \_ \_**   | 0x4   | Das UI-Plug-in ist ein Einstellungsbereich-Plug-in.        |
| **Plug-in- \_ \_ METADATAAREA**   | 0x5   | Das UI-Plug-in ist ein Metadatenbereich-Plug-in.        |



 

In der folgenden Tabelle werden die Flags für Plug-in-Funktionen erläutert.



| Flag für Plug-in-Funktionen             | Wert      | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                         |
|---------------------------------------|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Plug-in- \_ Flags- \_ Annahmen**       | 0x10000000 | Das UI-Plug-in kann **Medien** Objekt-Zeiger Arrays akzeptieren, wenn Windows Media Player " [**iwmppluginui:: SetProperty**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-setproperty) " aufruft.                                                                                                                                                                                                                                                           |
| **Plug-in- \_ Flags " \_ akzeptsplaylists"**   | 0x8000000  | Das UI-Plug-in kann **Listen Objekt-** Zeiger Arrays akzeptieren, wenn Windows Media Player " [**iwmppluginui:: SetProperty**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-setproperty) " aufruft.                                                                                                                                                                                                                                                        |
| **Plug-Ins für Plug-Ins \_ \_**         | 0x4000000  | Das UI-Plug-in verwendet Voreinstellungen. Wenn das Plug-in dieses Flag angibt, fragt Windows Media Player das Plug-in nach voreingestellten Informationen ab, indem [**iwmppluginui:: GetProperty**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-getproperty) aufgerufen wird.                                                                                                                                                                                                      |
| **Plug-in- \_ Flags \_ haspropertypage**    | 0x80000000 | Das UI-Plug-in enthält ein Dialogfeld für eine Eigenschaften Seite. Windows Media Player ruft [**iwmppluginui::D isplaypropertypage**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-displaypropertypage) auf, wenn dieses Flag festgelegt wird, wenn die Eigenschaften Seite aufgerufen wird.                                                                                                                                                                                                 |
| **\_ \_ ausgeblendet**             | 0x02000000 | Das Plug-in für die Benutzeroberfläche für die Benutzeroberfläche wird nicht im Menü **Plug-ins** angezeigt, auf das Sie über die Menüs **Ansicht** oder **Tools** oder die Schaltfläche **jetzt Wiedergabe Optionen auswählen** in der Wiedergabeliste zugreifen. Er wird im Dialogfeld Optionen auf der Registerkarte **Plug-ins** angezeigt. Dies bewirkt, dass das Plug-in für die Hintergrund Ausführung in der Statusleiste angezeigt wird. Dieses Flag hat keine Auswirkung auf Plug-ins, die keine background-UI-Plug-ins sind.<br/> |
| **Plug \_ \_ -in-Flags installautorun**     | 0x40000000 | Windows Media Player führt das UI-Plug-in automatisch aus, wenn das Plug-in installiert ist.                                                                                                                                                                                                                                                                                                                               |
| **Plug-in- \_ Flags \_ launchpropertypage** | 0x20000000 | Windows Media Player ruft [**iwmppluginui::D isplaypropertypage**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-displaypropertypage) auf, wenn das UI-Plug-in zum ersten Mal ausgeführt wird. Wenn dieses Flag angegeben ist, sollten die Plug-in- **\_ Flags \_ haspropertypage** ebenfalls angegeben werden.<br/>                                                                                                                                                             |



 

Die folgenden Konstanten sind in wmpplug. h definiert. Ändern Sie nicht die Werte, die diesen Konstanten zugeordnet sind.



| Name                                    | BESCHREIBUNG                               |
|-----------------------------------------|-------------------------------------------|
| **Plug-in- \_ installregkey**               | Der Speicherort des Plug-in-Registrierungsschlüssels. |
| **Plug-in \_ installregkey \_ FriendlyName** | Der Name des benutzerfreundlichen namens Werts.      |
| **Plug-in- \_ installregkey \_**  | Der Name des Beschreibungs Werts.        |
| **installregkey-Plug-in \_ \_** | Der Name des Funktions Werts.       |
| **Plug-in \_ installregkey \_ deinstallieren**    | Der Name des Deinstallations Pfad Werts.     |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Iwmppluginui::D isplaypropertypage**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-displaypropertypage)
</dt> <dt>

[**Iwmppluginui:: GetProperty**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-getproperty)
</dt> <dt>

[**Iwmppluginui:: SetProperty**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-setproperty)
</dt> <dt>

[**Programmier Referenz zu Benutzeroberflächen-Plug-ins**](user-interface-plug-ins-programming-reference.md)
</dt> </dl>

 

 





