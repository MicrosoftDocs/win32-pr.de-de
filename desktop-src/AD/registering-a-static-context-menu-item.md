---
title: Registrieren eines statischen Kontextmenü Elements
description: In diesem Thema wird beschrieben, wie ein statisches Kontextmenü Element registriert wird, das für Active Directory Objekte
ms.assetid: ed945812-3adb-4058-bdb6-8d9d34468265
ms.tgt_platform: multiple
keywords:
- Registrieren eines statischen Kontextmenü Elements AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89e3ee5336061ca296e2c94f8907ebd385610494
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "106338655"
---
# <a name="registering-a-static-context-menu-item"></a>Registrieren eines statischen Kontextmenü Elements

Die MMC-Snap-Ins "Verwaltung" von Active Directory Domain Services und der Windows-Shell bieten einen Mechanismus zum Hinzufügen eines Elements zum Kontextmenü, das für Objekte in Active Directory Domain Services angezeigt wird. Das Kontextmenü kann eine beliebige Datei aufrufen, die mit der [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) -API gestartet werden kann, z. b. eine Anwendungs-oder Webseiten-URL.

## <a name="registering-with-active-directory-domain-services"></a>Registrieren bei Active Directory Domain Services

Die Registrierung der Kontextmenüerweiterung ist spezifisch für ein Gebiets Schema. Wenn die Kontextmenüerweiterung auf alle Gebiets Schemas angewendet wird, muss Sie in allen Gebiets Schema-subcontainern im Container "Display Specifiers" im Objektklasse " [**displaySpecifier**](/windows/desktop/ADSchema/c-displayspecifier) " registriert werden. Wenn die Kontextmenüerweiterung für ein bestimmtes Gebiets Schema lokalisiert wird, muss Sie im **displaySpecifier** -Objekt in diesem Gebiets Schema-unter Container registriert werden. Weitere Informationen über die Anzeige spezifischere Container und Gebiets Schemas finden Sie unter [Anzeigen von Bezeichner](display-specifiers.md) und [displaySpecifier-Containern](displayspecifiers-container.md).

Es gibt zwei anzeigespezifiziererattribute, unter denen ein statisches Kontextmenü Element unter, [**adminContextMenu**](/windows/desktop/ADSchema/a-admincontextmenu) und [**shellcontextmenu**](/windows/desktop/ADSchema/a-shellcontextmenu)registriert werden kann.

Das [**adminContextMenu**](/windows/desktop/ADSchema/a-admincontextmenu) -Attribut identifiziert Verwaltungs Kontextmenüs, die in den administrativen Snap-Ins Active Directory Domain Services angezeigt werden. Das Kontextmenü wird angezeigt, wenn der Benutzer das Kontextmenü für Objekte der entsprechenden Klasse in einem der MMC-Snap-Ins "Verwaltung" anzeigt.

Das [**shellcontextmenu**](/windows/desktop/ADSchema/a-shellcontextmenu) -Attribut identifiziert Endbenutzer-Kontextmenüs, die in der Windows-Shell angezeigt werden. Das Kontextmenü wird angezeigt, wenn der Benutzer das Kontextmenü für Objekte der entsprechenden Klasse im Windows-Explorer anzeigt. Ab Windows Server 2003 werden von der Windows-Shell keine Objekte mehr aus Active Directory Domain Services angezeigt.

Alle diese Attribute sind mehr wertig.

Wenn Sie ein statisches Kontextmenü Element registrieren, benötigen die Werte für die Attribute " [**adminContextMenu**](/windows/desktop/ADSchema/a-admincontextmenu) " und " [**shellcontextmenu**](/windows/desktop/ADSchema/a-shellcontextmenu) " das folgende Format.


```C++
<order number>,<menu text>,<command>
```



" &lt; Order Number &gt; " ist eine nicht signierte Zahl, die die Position des Elements im Kontextmenü darstellt. Wenn ein Kontextmenü angezeigt wird, werden die Werte mithilfe eines Vergleichs der "Order Number"-Werte der einzelnen Werte sortiert &lt; &gt; . Wenn mehr als ein Wert dieselbe " &lt; Bestellnummer" aufweist &gt; , werden diese Kontextmenü Erweiterungen in der Reihenfolge geladen, in der Sie vom Active Directory Server gelesen werden. Verwenden Sie nach Möglichkeit eine nicht vorhandene " &lt; Bestellnummer &gt; ", d. h. eine, die nicht von anderen Werten in der-Eigenschaft verwendet wurde. Es gibt keine vorgeschriebene Anfangsposition, und Lücken sind in der Sequenz " &lt; Order Number &gt; " zulässig.

Der " &lt; Menütext &gt; " ist die Zeichenfolge, die im Kontextmenü angezeigt wird. Der " &lt; Menütext &gt; " kann ein "&"-Zeichen enthalten, das dem Tastenkombinationen für das Menü Element vorangestellt ist. Dadurch wird das vorangegangene Zeichen unterstrichen. Wenn z. b. der " &lt; Menütext" " &gt; &Datei" ist, wird der Menütext als "file" angezeigt, das "f" wird unterstrichen, und "f" ist die Tastenkombination für das Menü Element.

Der &lt; Befehl "Command &gt; " ist das Programm oder die Datei, die vom Snap-in ausgeführt wird. Entweder muss der vollständige Pfad angegeben werden, oder die Datei muss in der Computer Pfad-Umgebungsvariablen vorhanden sein. Die Datei wird mit der [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) -Funktion aufgerufen. Der &lt; Befehl "Command &gt; " kann keine zusätzlichen Parameter enthalten, z. b. Notepad.exe Myfile.txt. Da **ShellExecute** verwendet wird, können alle Dateien oder Adressen, die an **ShellExecute** übermittelt werden können, für " &lt; Command" verwendet werden &gt; . Wenn "Command" z. b. &lt; &gt; "d: \\file.txt" enthält, wird "d: \\file.txt" mit der Anwendung geöffnet, die mit der Erweiterung ". txt" verknüpft ist. Wenn " &lt; Command &gt; " "" enthält https://www.fabrikam.com , wird auch der Standard Webbrowser geöffnet, und die angegebene Webseite wird angezeigt. Pfade und Anwendungsnamen mit Leerzeichen sind zulässig. Wenn " &lt; Command &gt; " eine Anwendung ist, werden der ADsPath und die Klasse des ausgewählten Objekts als Befehlszeilenargumente, getrennt durch ein Leerzeichen, übermittelt.

In der Windows-Shell werden Kontextmenü Elemente mit Mehrfachauswahl unterstützt. In diesem Fall &lt; &gt; wird für jedes ausgewählte Objekt der Befehl "Command" aufgerufen. In Active Directory Domain Services ' Administrative Snap-Ins ' werden statische Kontextmenü Elemente mit Mehrfachauswahl nicht unterstützt.

> [!IMPORTANT]
> Bei der Windows-Shell werden Anzeige spezifiziererdaten bei der Benutzeranmeldung abgerufen und für die Benutzersitzung zwischengespeichert. Bei den administrativen Snap-Ins werden die Anzeige spezifiziererdaten abgerufen, wenn das Snap-In geladen und für die Dauer des Prozesses zwischengespeichert wird. Bei der Windows-Shell bedeutet dies, dass Änderungen an Anzeige spezifiken wirksam werden, nachdem sich ein Benutzer ab-und wieder anmeldet. Bei den administrativen Snap-Ins werden die Änderungen wirksam, wenn das Snap-in oder die Konsolen Datei erneut geladen wird. Das heißt, wenn Sie eine neue Instanz der Konsolen Datei oder eine neue Mmc.exe Instanz starten und das Snap-in hinzufügen, wird die aktuelle Anzeige spezifiziererdaten abgerufen.

 

Weitere Informationen und ein Codebeispiel finden Sie unter [Beispielcode für die Installation eines statischen Kontextmenü Elements](example-code-for-installing-a-static-context-menu-item.md).

 

 