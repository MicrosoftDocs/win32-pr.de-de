---
title: Kernimplementierung
description: 'Ein ADSI-Anbieter unterstützt die folgenden Features:'
ms.assetid: 39798237-a181-43b4-8441-ac711f923d4d
ms.tgt_platform: multiple
keywords:
- AdsI-Kernimplementierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d78487b701cac0409745ed3a7776dd882f2c37a878dec1d144c3b52a426db487
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118962089"
---
# <a name="core-implementation"></a>Kernimplementierung

Ein ADSI-Anbieter unterstützt die folgenden Features:

-   ADsPath-Zeichenfolgen im COM- und URL-Format. Definitionsgemäß können Sie ein Active Directory-Objekt mithilfe eines ADsPath abrufen. Anbieter unterstützen die Syntax, die ihr Verzeichnisdienst erfordert, indem sie **die ParseDisplayName-Implementierung** verwenden.
-   Ein Namespace-Objekt der obersten Ebene, das [**IParseDisplayName::P arseDisplayName**](/windows/win32/api/oleidl/nf-oleidl-iparsedisplayname-parsedisplayname) und [**IADsOpenDSObject unterstützt.**](/windows/desktop/api/Iads/nn-iads-iadsopendsobject) Dieses Objekt enthält die Stammknoten für diesen Namespace. Ein Teil der **ParseDisplayName-Implementierung** muss einen Parser enthalten, der auf Syntaxfehler für seinen eigenen Namespace überprüft. Dieses Objekt muss auch [**IADs und**](/windows/desktop/api/Iads/nn-iads-iads) **IADsOpenDSObject unterstützen.**
-   Die [**IADs-Schnittstelle.**](/windows/desktop/api/Iads/nn-iads-iads) Dies schließt eine einfache Implementierung des Eigenschaftencaches über [**IADs::GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) und [**IADs::SetInfo ein.**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) Vorgänge, die Objekteigenschaften erhalten oder festlegen, erfolgen im zwischengespeicherten Modus. Cachewerte werden während **IADs::SetInfo** in den zugrunde liegenden Verzeichnisspeicher geschrieben. Eine ADSI-Methode wird jedoch nicht zwischengespeichert, sondern sofort ausgeführt.
-   Die [**Schnittstellen IADsPropertyList,**](/windows/desktop/api/Iads/nn-iads-iadspropertylist) [**IADsPropertyEntry**](/windows/desktop/api/Iads/nn-iads-iadspropertyentry) und [**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue) für den direkten Zugriff auf und das Aufzählen der Eigenschaften im Eigenschaftencache. Bei Verzeichnisdiensten, die kein Schema verfügbar machen, können Sie mit dieser Schnittstelle die Eigenschaften eines Objekts bearbeiten.
-   Die [**IDirectoryObject-Schnittstelle**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) für Nichtautomatisierungsclients. Dabei wird das Over-the-Wire-Protokoll verwendet, um maximale Leistung zu erzielen, und der Eigenschaftencache wird umgangen.
-   Die [**IADsContainer-Schnittstelle.**](/windows/desktop/api/Iads/nn-iads-iadscontainer) Jedes Active Directory-Objekt verfügt über einen übergeordneten Container, der seine Lebensdauer steuert. Beachten Sie, dass sich [**IADs::GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) für ADs-Containerobjekte nur auf die Containereigenschaften und nicht auf deren Inhalt auswirken. SetInfo für ADs-Containerobjekte wirkt sich nur auf die Containereigenschaften aus und wirkt sich nicht auf neu erstellte Objekte oder Objekte aus, die bereits im Container vorhanden sind.
-   Die [**IDispatch-Schnittstelle.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) Dies ist die Automatisierungsschnittstelle für Sprachen wie Visual Basic Scripting Edition, die keine Kompilierzeitbindung verwenden. Im Zusammenhang damit stehen die Typbibliotheksdaten, die ein Anbieter zur Verfügung stehen muss. Weitere Informationen finden Sie unter [Implementierungsprobleme für ADSI-Anbieter.](implementation-issues-for-adsi-providers.md)
-   Ein Schemaklassencontainerobjekt und die entsprechenden Syntax-, Eigenschafts- und Schemaklassenobjekte, die [**IADsSyntax,**](/windows/desktop/api/Iads/nn-iads-iadssyntax) [**IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty)bzw. [**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass) unterstützen. Jeder Stammknoten muss mindestens ein eigenes Schemaklassencontainerobjekt enthalten.
-   Die [**IADsMembers-Schnittstelle,**](/windows/desktop/api/Iads/nn-iads-iadsmembers) wenn unterstützte Attribute Sammlungen von ADSI-Objekten sind, z. B. Sicherheitsgruppen.
-   Die [**IADsCollection-Schnittstelle,**](/windows/desktop/api/Iads/nn-iads-iadscollection) wenn unterstützte Attribute Sammlungen desselben Verzeichniselementtyps mit der Funktion [**IADsCollection::Add**](/windows/desktop/api/Iads/nf-iads-iadscollection-add) und [**IADsCollection::Remove**](/windows/desktop/api/Iads/nf-iads-iadscollection-remove) sind.
-   Die **IEnumXXXX-Enumeration** unterstützt alle spezifischen Enumeratorobjekte.
-   Routinen zum Zuordnen von Syntax und Konvertieren nativer Daten in den [**VARIANT-Datentyp.**](/windows/win32/api/oaidl/ns-oaidl-variant)
-   Befolgen Sie die ADSI-Konventionen für vom Anbieter bereitgestellte ADSI-Objekte. Schließen Sie Hilfedateien und Typbibliotheken ein, die die Schnittstelleneigenschaften und -methoden dokumentieren.

Wie bei jeder COM-Implementierung müssen Aufrufe von [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) **E \_ NOINTERFACE** für nicht implementierte Schnittstellen zurückgeben, **E \_ NOTIMPL** für nicht implementierte Methoden von Schnittstellen, die andernfalls implementiert werden, und **E ADS PROPERTY NOT \_ \_ \_ \_ SUPPORTED** für nicht implementierte Eigenschaften zurückgeben. Weitere Informationen zu dualen Schnittstellen und deren Auswirkungen auf die Implementierung von Eigenschaften finden Sie unter [Duale Schnittstellen](dual-interfaces.md).

 

 