---
title: Benutzerdefinierte Schriftart Auflistungen (Windows 7/8)
description: DirectWrite ermöglicht mithilfe der getsystemfontcollection-Methode von idschreitefactory den Zugriff auf die System Schriftart Auflistung.
ms.assetid: ec892904-6778-4fbd-93b4-62d0db5b82ea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39aa764330f27b72051ef682c6ce5f1176c42c7d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728681"
---
# <a name="custom-font-collections-windows-78"></a>Benutzerdefinierte Schriftart Auflistungen (Windows 7/8)

[DirectWrite](direct-write-portal.md) ermöglicht mithilfe der [**idwrite-Factory:: getsystemfontcollection**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-getsystemfontcollection) -Methode den Zugriff auf die System Schriftart Auflistung. Dies ist die am häufigsten verwendete Schriftart Auflistung. Einige Anwendungen müssen jedoch Schriftarten verwenden, die nicht auf dem System installiert sind, z. b. aus enthaltenen Schriftart Dateien oder Schriftart Dateien, die in die Anwendung eingebettet sind.

Wenn sich die gewünschten Schriftarten nicht in der System Schriftart Auflistung befinden, können Sie eine benutzerdefinierte Schriftart Sammlung erstellen, die von " [**idschreitefontcollection**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection)" abgeleitet ist.

Diese Übersicht besteht aus den folgenden Teilen:

-   [Registrieren und Aufheben der Registrierung eines Schriftart Sammlungs Lade Moduls](#registering-and-unregistering-a-font-collection-loader)
-   [Idschreitefontcollectionloader](#idwritefontcollectionloader)
-   [Idschreitefontfileenumerator](#idwritefontfileenumerator)
-   ["Kreatecustomfontfilereferenzierung"](#createcustomfontfilereference)
-   [Idschreitefontfileloader](#idwritefontfileloader)
-   [Idschreitefontfilestream](#idwritefontfilestream)

## <a name="registering-and-unregistering-a-font-collection-loader"></a>Registrieren und Aufheben der Registrierung eines Schriftart Sammlungs Lade Moduls

Sie registrieren ein Schriftart Sammlungs Lade Tool mithilfe der [**idwrite-Factory:: registerfontcollectionloader**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-registerfontcollectionloader) -Methode, und übergeben Sie eine [**idschreitefontcollectionloader**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollectionloader) -Schnittstelle, die von der Anwendung als Singleton-Objekt implementiert wird. Dieses Objekt lädt die Schriftarten, wenn die benutzerdefinierte Auflistung angefordert wird. Sowohl die System Schriftart Auflistung als auch benutzerdefinierte Schriftart Sammlungen werden zwischengespeichert, sodass die Schriftarten nur einmal geladen werden.

Das Schriftart Sammlungs Lade Tool muss schließlich mithilfe von [**idwrite-Factory:: unregisterfontcollectionloader**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-unregisterfontcollectionloader)entladen werden.

> [!Note]  
> Beim Registrieren des Lade Moduls für Schriftart Sammlungen wird der Verweis Zähler hinzugefügt. [**unregisterfontcollectionloader**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-unregisterfontcollectionloader) kann nicht innerhalb des Dekonstruktors aufgerufen werden, oder das Auflistungs Lade Objekt wird nie die Registrierung aufheben.

 

## <a name="idwritefontcollectionloader"></a>Idschreitefontcollectionloader

Sie erstellen ein [**idwrite-fontfileenumerator**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileenumerator) -Objekt, indem Sie die [**idwrite-Factory:: anatecustomfontcollection**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createcustomfontcollection) verwenden und ihr einen Anwendungs definierten Schlüssel übergeben. Der Schlüssel ist ein void-Zeiger, und der Datentyp, das Format und die Bedeutung werden von der Anwendung definiert und sind für das Schriftart System nicht transparent.

Der Schlüssel kann ein beliebiger Schlüssel sein, aber für [DirectWrite](direct-write-portal.md) ist Folgendes erforderlich:

-   Eindeutig für eine einzelne Schriftart Auflistung innerhalb des Gültigkeits Bereichs des Lade Moduls.
-   Gültig, bis die Registrierung des Lade Moduls mithilfe der Factory aufgehoben wird.

Wenn die Methode " [**samatecustomfontcollection**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createcustomfontcollection) " aufgerufen wird, ruft [DirectWrite](direct-write-portal.md) an eine [**idschreitefontcollectionloader**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollectionloader) -Schnittstelle zurück, die von der Anwendung als Singleton-Objekt implementiert wird. Die [**idwrite-fontcollectionloader::**](/windows/win32/api/dwrite/nf-dwrite-idwritefontcollectionloader-createenumeratorfromkey) -Rückruf Methode wird von DirectWrite zum Abrufen eines [**idwrite-fontfileenumerator**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileenumerator) -Objekts verwendet, das von der Anwendung implementiert wird. Das [**idwrite-Factory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) -Objekt, das zum Erstellen der Auflistung verwendet wird, wird an diese Methode übermittelt und sollte vom Schriftart Datei-Enumerator verwendet werden, um die [**idwrite-fontfile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile) -Objekte zu erstellen, die in die Auflistung eingeschlossen werden sollen.

Der an diese Methode über gegebene Schlüssel identifiziert die Schriftart Auflistung und ist derselbe Schlüssel, der an die Datei " [**kreatecustomfontcollection**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createcustomfontcollection)" übergeben wird.

## <a name="idwritefontfileenumerator"></a>Idschreitefontfileenumerator

Das Anwendungs definierte [**idwrite-fontfileenumerator**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileenumerator) -Objekt, das von der Methode " [**forateenumeratorfromkey**](/windows/win32/api/dwrite/nf-dwrite-idwritefontcollectionloader-createenumeratorfromkey) " erstellt wurde, wird zum Auflisten der Schriftart Dateien in einer Auflistung verwendet und erstellt ein [**idwrite-fontfile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile) -Objekt für jede Datei. Die [**idwrite-fontfileenumerator:: arvenext**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfileenumerator-movenext) -Methode ändert die Position in die nächste Schriftart Datei. Wenn an der Position eine Datei vorhanden ist, wird " *hascurrentfile* " auf " **true**" festgelegt. Andernfalls wird Sie auf " **false** " festgelegt, und die Methode gibt " **S \_ OK**" zurück.

> [!Note]  
> Der Enumerator für Schriftart Dateien muss vor dem ersten Element positioniert und beim ersten-Befehl von " [**muvenext**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfileenumerator-movenext)" erweitert werden.

 

Ein [**idwrite-fontfile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile) -Objekt wird von der [**idschreitefontfileenumerator:: getcurrentfontfile**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfileenumerator-getcurrentfontfile) -Methode ausgegeben. Wenn an der aktuellen Position keine Schriftart Datei vorhanden ist, da " [**muvenext**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfileenumerator-movenext) " noch nicht aufgerufen wurde oder hascurrentfile auf **false** festgelegt wurde, gibt **getcurrentfontfile** den Wert **E \_ Fail** zurück.

## <a name="createcustomfontfilereference"></a>"Kreatecustomfontfilereferenzierung"

Das [**idwrite-fontfile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile) -Objekt, das von [**getcurrentfontfile**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfileenumerator-getcurrentfontfile) ausgegeben wird, kann durch Aufrufen von " [**idwrite tefactory:: createcustomfontfilereferenzierung**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createcustomfontfilereference)" erstellt werden. Der Verweis Schlüssel der Schriftart Datei identifiziert einen bestimmten Schriftart Datei Verweis und muss innerhalb des Schriftart Datei Lade Moduls eindeutig sein, das die Datei lädt.

## <a name="idwritefontfileloader"></a>Idschreitefontfileloader

Die Methode " [**kreatecustomfontfilereferenzierung**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createcustomfontfilereference) " nimmt ein von der Anwendung implementiertes [**idschreitefontfileloader**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileloader) -Objekt an, das zum Laden der Schriftart verwendet wird. Der " [**idwrite:: deestreamfromkey**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfileloader-createstreamfromkey) "-Rückruf Methode wird der Schlüssel übergeben und ein " [**idschreitefontfilestream**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfilestream) "-Objekt ausgegeben.

## <a name="idwritefontfilestream"></a>Idschreitefontfilestream

Das von der Anwendung implementierte [**idschreitefontfilestream**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfilestream) -Objekt stellt die Schriftart Datei Daten für einen Schriftart Datei Verweis von einem benutzerdefinierten Schriftart Datei Lade Tool bereit. Zusammen mit der Dateigröße und dem Zeitpunkt des letzten Schreibvorgangs stellt Sie eine Methode ("[**infofilefragment**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfilestream-readfilefragment)") zum Abrufen von Datei Fragmenten bereit, die in ein " [**idschreitefontfile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile) "-Objekt kompiliert werden sollen.

> [!Note]  
> Die Implementierung von "read [**filefragment**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfilestream-readfilefragment) " sollte einen Fehler zurückgeben, wenn das angeforderte Fragment außerhalb der Datei Begrenzungen liegt.

 

Ein [**idwrite-fontfilestream**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfilestream) kann den Inhalt der Schriftart Datei von einem beliebigen Standort aus aufrufen, z. b. von der lokalen Festplatte oder von eingebetteten Ressourcen.

 

 