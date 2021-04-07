---
title: Registrieren des Kontextmenü-com-Objekts in einem Anzeigespezifizierer
description: In diesem Thema werden die Registrierungsschlüssel erläutert, die zum Registrieren eines COM-Objekts für das Kontextmenü geändert werden müssen.
ms.assetid: 389bc249-4849-4763-9d1b-b35598a51050
ms.tgt_platform: multiple
keywords:
- Registrieren des Kontextmenü-com-Objekts in einem Anzeigespezifizierer
- Kontextmenü-com-Objekt AD, registrieren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62ae30c1a60a1a0bc5a8ec388a3578ab13829c95
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104038737"
---
# <a name="registering-the-context-menu-com-object-in-a-display-specifier"></a>Registrieren des Kontextmenü-com-Objekts in einem Anzeigespezifizierer

Wenn Sie com zum Erstellen einer Kontextmenü-Erweiterungs-DLL für einen Active Directory Verzeichnisdienst verwenden, muss die Erweiterung bei der Windows-Registrierung registriert und Active Directory Domain Services werden, um die Active Directory Verwaltungs-MMC-Snap-Ins und die Windows-Shell der Erweiterung zu benachrichtigen.

## <a name="registering-in-the-windows-registry"></a>Registrieren in der Windows-Registrierung

Wie alle com-Server muss eine Kontextmenüerweiterung in der Registrierung registriert werden. Die Erweiterung wird unter dem folgenden Schlüssel registriert.

```
HKEY_CLASSES_ROOT
   CLSID
      <clsid>
```

*<clsid>* die Zeichen folgen Darstellung der CLSID, die von der [**stringfromclsid**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) -Funktion erstellt wird. Unter dem *<clsid>* Schlüssel gibt es einen **InProcServer32** -Schlüssel, der das-Objekt als 32-Bit-in-proc-Server identifiziert. Unter der **InProcServer32** -Taste wird der Speicherort der dll im Standardwert angegeben, und das Threading Modell wird im **ThreadingModel** -Wert angegeben. Alle Kontextmenü Erweiterungen müssen das Threading Modell "Apartment" verwenden.

## <a name="registering-with-active-directory-domain-services"></a>Registrieren bei Active Directory Domain Services

Die Registrierung der Kontextmenüerweiterung ist spezifisch für ein Gebiets Schema. Wenn die Kontextmenüerweiterung auf alle Gebiets Schemas angewendet wird, muss Sie in allen Gebiets Schema-subcontainern im Container "Display Specifiers" im Objektklasse " [**displaySpecifier**](/windows/desktop/ADSchema/c-displayspecifier) " registriert werden. Wenn die Kontextmenüerweiterung für ein bestimmtes Gebiets Schema lokalisiert wird, muss Sie im **displaySpecifier** -Objekt im unter Container dieses Gebiets Schemas registriert werden. Weitere Informationen über die Anzeige spezifischere Container und Gebiets Schemas finden Sie unter [Anzeigen von Bezeichner](display-specifiers.md) und [displaySpecifier-Containern](displayspecifiers-container.md).

Es gibt zwei anzeigespezifiziererattribute, unter denen ein Kontextmenü-Erweiterungs Element registriert werden kann. Dies sind " [**adminContextMenu**](/windows/desktop/ADSchema/a-admincontextmenu) " und " [**shellcontextmenu**](/windows/desktop/ADSchema/a-shellcontextmenu)".

Das [**adminContextMenu**](/windows/desktop/ADSchema/a-admincontextmenu) -Attribut identifiziert Verwaltungs Kontextmenüs, die in Active Directory administrativen Snap-Ins angezeigt werden. Das Kontextmenü wird angezeigt, wenn der Benutzer das Kontextmenü für Objekte der entsprechenden Klasse in einem der Active Directory-Verwaltungs-MMC-Snap-Ins anzeigt.

Das [**shellcontextmenu**](/windows/desktop/ADSchema/a-shellcontextmenu) -Attribut identifiziert Endbenutzer-Kontextmenüs, die in der Windows-Shell angezeigt werden. Das Kontextmenü wird angezeigt, wenn der Benutzer das Kontextmenü für Objekte der entsprechenden Klasse im Windows-Explorer anzeigt. Ab Windows Server 2003 zeigt die Windows-Shell keine Objekte Active Directory Domain Services mehr an.

Alle diese Attribute sind mehr wertig.

Beim Registrieren einer Kontextmenüerweiterung benötigen die Werte für die Attribute " [**adminContextMenu**](/windows/desktop/ADSchema/a-admincontextmenu) " und " [**shellcontextmenu**](/windows/desktop/ADSchema/a-shellcontextmenu) " das folgende Format.


```C++
<order number>,<clsid>
```



" &lt; Order Number &gt; " ist eine nicht signierte Zahl, die die Position des Elements im Kontextmenü darstellt. Wenn ein Kontextmenü angezeigt wird, werden die Werte mithilfe eines Vergleichs der "Order Number"-Werte der einzelnen Werte sortiert &lt; &gt; . Wenn mehr als ein Wert dieselbe " &lt; Bestellnummer" aufweist &gt; , werden diese Kontextmenü Erweiterungen in der Reihenfolge geladen, in der Sie vom Active Directory Server gelesen werden. Verwenden Sie nach Möglichkeit eine nicht vorhandene " &lt; Bestellnummer &gt; ", d. h. eine, die nicht von anderen Werten in der-Eigenschaft verwendet wurde. In der &lt; Sequenz "Order Number" sind keine vorgeschriebenen Startpositionen und Lücken zulässig &gt; .

Die " &lt; CLSID &gt; " ist die Zeichen folgen Darstellung der CLSID, die von der [**stringfromclsid**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) -Funktion erstellt wird.

In der Windows-Shell werden Kontextmenü Elemente mit Mehrfachauswahl unterstützt. In diesem Fall wird die Kontextmenüerweiterung für jedes ausgewählte Objekt aufgerufen. In Active Directory administrativen Snap-Ins werden auch Mehrfachauswahl-Kontextmenü Erweiterungs Elemente unterstützt. In diesem Fall enthält die [**dsobjectnames**](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames) -Struktur für jedes ausgewählte Verzeichnis Objekt eine [**dsobject**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject) -Struktur.

> [!IMPORTANT]
> Bei der Windows-Shell werden Anzeige spezifiziererinformationen bei der Benutzeranmeldung abgerufen und für die Benutzersitzung zwischengespeichert. Bei den administrativen Snap-Ins werden die Anzeige spezifiziererdaten abgerufen, wenn das Snap-In geladen und für die Dauer des Prozesses zwischengespeichert wird. Bei der Windows-Shell bedeutet dies, dass Änderungen an Anzeige spezifiken wirksam werden, nachdem sich ein Benutzer ab-und wieder anmeldet. Bei den administrativen Snap-Ins werden die Änderungen wirksam, wenn das Snap-in oder die Konsolen Datei erneut geladen wird. das heißt, wenn Sie eine neue Instanz der Konsolen Datei oder eine neue Mmc.exe Instanz starten und das Snap-in hinzufügen, werden die aktuellen anzeigespezifiziererdaten abgerufen.

 

Weitere Informationen und ein Codebeispiel für die Implementierung einer Kontextmenüerweiterung finden Sie unter [Beispielcode für die Implementierung des Kontextmenü-com-Objekts](example-code-for-implementation-of-the-context-menu-com-object.md).

 

 