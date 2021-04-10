---
title: Core-Implementierung
description: 'Ein ADSI-Anbieter unterstützt die folgenden Features:'
ms.assetid: 39798237-a181-43b4-8441-ac711f923d4d
ms.tgt_platform: multiple
keywords:
- Core-Implementierung ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f62068bd77553f89e222422431811da1ef251ccd
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104039609"
---
# <a name="core-implementation"></a>Core-Implementierung

Ein ADSI-Anbieter unterstützt die folgenden Features:

-   ADsPath-Zeichen folgen im com-und URL-Format. Definitionsgemäß können Sie ein Active Directory Objekt mithilfe eines ADsPath-Objekts abrufen. Anbieter unterstützen die Syntax, die ihr Verzeichnisdienst erfordert, indem Sie die Implementierung von " **parameyname** " verwenden.
-   Ein Namespace Objekt der obersten Ebene, das [**iparamesedisplayname::P arsedisplayname**](/windows/win32/api/oleidl/nf-oleidl-iparsedisplayname-parsedisplayname) und [**iadsopendsobject**](/windows/desktop/api/Iads/nn-iads-iadsopendsobject)unterstützt. Dieses Objekt enthält die Stamm Knoten für diesen Namespace. Ein Teil der **parmendisplayname** -Implementierung muss einen Parser enthalten, der auf Syntax Fehler für einen eigenen Namespace prüft. Dieses Objekt muss auch [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) und **iadsopendsobject** unterstützen.
-   Die [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) -Schnittstelle. Dies umfasst eine einfache Implementierung des Eigenschafts Caches über [**IADs:: GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) und [**IADs:: abtinfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo). Vorgänge, bei denen Objekteigenschaften im Modus mit Zwischenspeicherung angezeigt oder festgelegt werden. Cache Werte werden in den zugrunde liegenden Verzeichnis Speicher geschrieben, während **IADs:: abfo**. Eine ADSI-Methode wird jedoch nicht zwischengespeichert, sondern sofort ausgeführt.
-   Die [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist)-, [**iadspropertyentry**](/windows/desktop/api/Iads/nn-iads-iadspropertyentry) -und [**iadspropertyvalue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue) -Schnittstellen für den direkten Zugriff auf und das Auflisten der Eigenschaften im Eigenschaften Cache. Für Verzeichnisdienste, die kein Schema verfügbar machen, können Sie mithilfe dieser Schnittstelle die Eigenschaften eines Objekts bearbeiten.
-   Die [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) -Schnittstelle für nicht-Automatisierungs Clients. Dabei wird das Protokoll über das Netzwerk für maximale Leistung verwendet und der Eigenschafts Cache umgangen.
-   Die [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) -Schnittstelle. Jedes Active Directory Objekt verfügt über einen übergeordneten Container, der seine Lebensdauer steuert. Beachten Sie, dass sich [**IADs:: GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) bei ADS-Container Objekten nur auf die Container Eigenschaften und nicht auf ihren Inhalt auswirkt. SetInfo on ADS Container Objects wirkt sich nur auf die Container Eigenschaften aus und wirkt sich nicht auf neu erstellte Objekte oder Objekte aus, die bereits im Container vorhanden sind.
-   Die [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle. Dies ist die Automatisierungsschnittstelle für Sprachen wie Visual Basic Scripting Edition, die keine Kompilierzeit Bindung verwenden. Dabei handelt es sich um die Typbibliotheks Daten, die von einem Anbieter bereitgestellt werden müssen. Weitere Informationen finden Sie unter [Implementierungsprobleme bei ADSI-Anbietern](implementation-issues-for-adsi-providers.md).
-   Ein Container Objekt der Schema Klasse und die entsprechenden Syntax-, Eigenschafts-und Schema Klassen Objekte, die [**iadssyntax**](/windows/desktop/api/Iads/nn-iads-iadssyntax), [**iadsproperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty)und [**iadsclass**](/windows/desktop/api/Iads/nn-iads-iadsclass) unterstützen. Jeder Stamm Knoten muss mindestens ein eigenes Schema Klassencontainer-Objekt enthalten.
-   Die [**iadsmembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers) -Schnittstelle, wenn unterstützte Attribute Sammlungen von ADSI-Objekten sind, z. b. Sicherheitsgruppen.
-   Die [**iadscollection**](/windows/desktop/api/Iads/nn-iads-iadscollection) -Schnittstelle, wenn es sich bei allen unterstützten Attributen um Auflistungen desselben Verzeichnis Elementtyps mit [**iadscollection:: Add**](/windows/desktop/api/Iads/nf-iads-iadscollection-add) -und [**iadscollection:: Remove**](/windows/desktop/api/Iads/nf-iads-iadscollection-remove) -Funktion handelt.
-   Die **IEnumXXXX** -Enumeration unterstützt alle spezifischen Enumeratorobjekte.
-   Routinen, um die Syntax zuzuordnen und systemeigene Daten in den [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) -Datentyp zu konvertieren.
-   Befolgen Sie die ADSI-Konventionen für vom Anbieter bereitgestellte ADSI-Objekte. Einschließen von Hilfedateien und Typbibliotheken, die die Schnittstelleneigenschaften und-Methoden dokumentieren.

Wie bei jeder com-Implementierung müssen Aufrufe von [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) **e \_ nointerface** für nicht implementierte Schnittstellen zurückgeben, **e \_ notifimpl** für nicht implementierte Methoden von Schnittstellen, die anderweitig implementiert werden und die e ADS-Eigenschaft zurückgeben, die für nicht implementierte Eigenschaften **\_ \_ \_ nicht \_ unterstützt** wird. Weitere Informationen über duale Schnittstellen und deren Auswirkung auf die Eigenschaften Implementierung finden Sie unter [duale Schnittstellen](dual-interfaces.md).

 

 