---
title: Registrieren des COM-Kontextmenüobjekts in einem Anzeigespezifizierer
description: In diesem Thema werden die Registrierungsschlüssel gezeigt, die geändert werden müssen, um ein COM-Kontextmenüobjekt zu registrieren.
ms.assetid: 389bc249-4849-4763-9d1b-b35598a51050
ms.tgt_platform: multiple
keywords:
- Registrieren des COM-Kontextmenüobjekts in einem Anzeigespezifizierer
- Kontextmenü COM-Objekt AD , registrieren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c5650d5864093293728e5c4f1157980c76bffa0
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881243"
---
# <a name="registering-the-context-menu-com-object-in-a-display-specifier"></a>Registrieren des COM-Kontextmenüobjekts in einem Anzeigespezifizierer

Wenn Sie COM verwenden, um eine Kontextmenüerweiterungs-DLL für einen Active Directory-Verzeichnisdienst zu erstellen, muss die Erweiterung bei der Windows-Registrierung registriert und Active Directory Domain Services werden, um die MMC-Snap-Ins der Active Directory-Verwaltung und die Windows Shell der Erweiterung zu benachrichtigen.

## <a name="registering-in-the-windows-registry"></a>Registrieren in der Windows Registry

Wie alle COM-Server muss eine Kontextmenüerweiterung in der Registrierung registriert werden. Die Erweiterung wird unter dem folgenden Schlüssel registriert.

```
HKEY_CLASSES_ROOT
   CLSID
      <clsid>
```

*&lt; clsid &gt;* ist die Zeichenfolgendarstellung der CLSID, die von der [**StringFromCLSID-Funktion**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) erzeugt wird. Unter dem *&lt; Schlüssel &gt; clsid* befindet sich ein **InProcServer32-Schlüssel,** der das Objekt als 32-Bit-Prozessserver identifiziert. Unter dem **InProcServer32-Schlüssel** wird der Speicherort der DLL im Standardwert angegeben, und das Threadingmodell wird im **ThreadingModel-Wert** angegeben. Alle Kontextmenüerweiterungen müssen das Threadingmodell "Apartment" verwenden.

## <a name="registering-with-active-directory-domain-services"></a>Registrieren bei Active Directory Domain Services

Die Registrierung der Kontextmenüerweiterung ist spezifisch für ein Gebietsschema. Wenn die Kontextmenüerweiterung für alle Gebietsschemas gilt, muss sie in der Objektklasse [**displaySpecifier-Objekt**](/windows/desktop/ADSchema/c-displayspecifier) in allen Gebietsschemauntercontainern im Container Anzeigespezifizierer registriert werden. Wenn die Kontextmenüerweiterung für ein bestimmtes Gebietsschema lokalisiert ist, muss sie im **displaySpecifier-Objekt** im Untercontainer dieses Gebietsschemas registriert werden. Weitere Informationen zum Container "Anzeigespezifizierer" und zu gebietsschemas finden Sie unter [Anzeigespezifizierer](display-specifiers.md) und [DisplaySpecifiers-Container.](displayspecifiers-container.md)

Es gibt zwei Anzeigespezifiziererattribute, unter denen ein Kontextmenüerweiterungselement registriert werden kann. Dies sind [**adminContextMenu**](/windows/desktop/ADSchema/a-admincontextmenu) und [**shellContextMenu.**](/windows/desktop/ADSchema/a-shellcontextmenu)

Das [**adminContextMenu-Attribut**](/windows/desktop/ADSchema/a-admincontextmenu) identifiziert administrative Kontextmenüs, die in Active Directory-Administrator-Snap-Ins angezeigt werden sollen. Das Kontextmenü wird angezeigt, wenn der Benutzer das Kontextmenü für Objekte der entsprechenden Klasse in einem der MMC-Snap-Ins für die Active Directory-Verwaltung anzeigt.

Das [**shellContextMenu-Attribut**](/windows/desktop/ADSchema/a-shellcontextmenu) identifiziert Endbenutzerkontextmenüs, die in der Windows Shell angezeigt werden sollen. Das Kontextmenü wird angezeigt, wenn der Benutzer das Kontextmenü für Objekte der entsprechenden Klasse im Windows-Explorer anzeigt. Ab Windows Server 2003 zeigt die Windows Shell keine Objekte von Active Directory Domain Services mehr an.

Alle diese Attribute sind mehrwertige Attribute.

Beim Registrieren einer Kontextmenüerweiterung benötigen die Werte für die Attribute [**adminContextMenu**](/windows/desktop/ADSchema/a-admincontextmenu) und [**shellContextMenu**](/windows/desktop/ADSchema/a-shellcontextmenu) das folgende Format.


```C++
<order number>,<clsid>
```



Die &lt; Bestellnummer &gt; ist eine Zahl ohne Vorzeichen, die die Elementposition im Kontextmenü darstellt. Wenn ein Kontextmenü angezeigt wird, werden die Werte mithilfe eines Vergleichs der "Bestellnummer" jedes Werts &lt; &gt; sortiert. Wenn mehr als ein Wert die gleiche &lt; "Bestellnummer" &gt; aufweist, werden diese Kontextmenüerweiterungen in der Reihenfolge geladen, in der sie vom Active Directory-Server gelesen werden. Verwenden Sie nach Möglichkeit eine nicht vorhandene &lt; "Bestellnummer", &gt; d. h. eine, die nicht von anderen Werten in der -Eigenschaft verwendet wurde. Es gibt keine vorgeschriebene Anfangsposition, und Lücken sind in der &lt; Sequenz "Bestellnummer" &gt; zulässig.

&lt;"clsid" &gt; ist die Zeichenfolgendarstellung der CLSID, die von der [**StringFromCLSID-Funktion**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) erzeugt wird.

In der Windows Shell werden Kontextmenüelemente mit mehrfacher Auswahl unterstützt. In diesem Fall wird die Kontextmenüerweiterung für jedes ausgewählte Objekt aufgerufen. In Active Directory-Administrator-Snap-Ins werden auch Kontextmenüerweiterungselemente mit mehrfacher Auswahl unterstützt. In diesem Fall enthält die [**DSOBJECTNAMES-Struktur**](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames) eine [**DSOBJECT-Struktur**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject) für jedes ausgewählte Verzeichnisobjekt.

> [!IMPORTANT]
> Für die Windows Shell werden Anzeigespezifiziererinformationen bei der Benutzeranmeldung abgerufen und für die Sitzung des Benutzers zwischengespeichert. Für die administrativen Snap-Ins werden die Anzeigespezifiziererdaten abgerufen, wenn das Snap-In geladen und für die Dauer des Prozesses zwischengespeichert wird. Für die Windows Shell bedeutet dies, dass Änderungen an Anzeigespezifizierern wirksam werden, nachdem sich ein Benutzer abgemeldet und wieder eingeschaltet hat. Für die administrativen Snap-Ins werden Änderungen wirksam, wenn das Snap-In oder die Konsolendatei neu geladen wird, d. h., wenn Sie eine neue Instanz der Konsolendatei oder eine neue Mmc.exe Instanz starten und das Snap-In hinzufügen, werden die neuesten Anzeigespezifiziererdaten abgerufen.

 

Weitere Informationen und ein Codebeispiel zum Implementieren einer Kontextmenüerweiterung finden Sie unter [Beispielcode für die Implementierung des COM-Kontextmenüobjekts.](example-code-for-implementation-of-the-context-menu-com-object.md)

 

 
