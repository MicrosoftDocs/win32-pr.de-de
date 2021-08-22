---
title: Benutzerdefinierte Schriftartauflistungen (Windows 7/8)
description: DirectWrite ermöglicht den Zugriff auf die Systemschriftartauflistung mithilfe der IDWriteFactory GetSystemFontCollection-Methode.
ms.assetid: ec892904-6778-4fbd-93b4-62d0db5b82ea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffc76214dda067b43c27c8e04e4419f147d0e33b7566b4dedc5ac3255a1c1dc9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119290760"
---
# <a name="custom-font-collections-windows-78"></a>Benutzerdefinierte Schriftartauflistungen (Windows 7/8)

[DirectWrite](direct-write-portal.md) ermöglicht den Zugriff auf die Systemschriftartauflistung mithilfe der [**IDWriteFactory::GetSystemFontCollection-Methode.**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-getsystemfontcollection) Dies ist die Schriftartenauflistung, die am häufigsten verwendet wird. Einige Anwendungen müssen jedoch Schriftarten verwenden, die nicht auf dem System installiert sind, z. B. aus eingeschlossenen Schriftartdateien oder in der Anwendung eingebetteten Schriftartdateien.

Wenn die gewünschten Schriftarten nicht in der Systemschriftartauflistung enthalten sind, können Sie eine benutzerdefinierte Schriftartsammlung erstellen, die von [**IDWriteFontCollection**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection)abgeleitet wird.

Diese Übersicht besteht aus den folgenden Teilen:

-   [Registrieren und Aufheben der Registrierung eines Schriftartauflistungsladeprogramm](#registering-and-unregistering-a-font-collection-loader)
-   [IDWriteFontCollectionLoader](#idwritefontcollectionloader)
-   [IDWriteFontFileEnumerator](#idwritefontfileenumerator)
-   [CreateCustomFontFileReference](#createcustomfontfilereference)
-   [IDWriteFontFileLoader](#idwritefontfileloader)
-   [IDWriteFontFileStream](#idwritefontfilestream)

## <a name="registering-and-unregistering-a-font-collection-loader"></a>Registrieren und Aufheben der Registrierung eines Schriftartauflistungsladeprogramm

Sie registrieren ein Ladeprogramm für die Schriftartauflistung mithilfe der [**IDWriteFactory::RegisterFontCollectionLoader-Methode**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-registerfontcollectionloader) und übergeben ihm eine [**IDWriteFontCollectionLoader-Schnittstelle,**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollectionloader) die von der Anwendung als Singletonobjekt implementiert wird. Dieses Objekt lädt die Schriftarten, wenn die benutzerdefinierte Auflistung angefordert wird. Sowohl die Systemschriftartauflistung als auch benutzerdefinierte Schriftartauflistungen werden zwischengespeichert, sodass die Schriftarten nur einmal geladen werden.

Das Ladeprogramm für die Schriftartauflistung muss schließlich mithilfe von [**IDWriteFactory::UnregisterFontCollectionLoader**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-unregisterfontcollectionloader)entladen werden.

> [!Note]  
> Das Registrieren des Ladeprogramm für die Schriftartauflistung wird dem Verweiszähler hinzugefügt. Rufen [**Sie unregisterFontCollectionLoader**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-unregisterfontcollectionloader) nicht innerhalb des Destruktors auf, da die Registrierung des Auflistungsladeprogrammobjekts nicht aufgehoben wird.

 

## <a name="idwritefontcollectionloader"></a>IDWriteFontCollectionLoader

Sie erstellen ein [**IDWriteFontFileEnumerator-Objekt,**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileenumerator) indem Sie [**idWriteFactory::CreateCustomFontCollection**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createcustomfontcollection) verwenden und ihm einen anwendungsdefiniert Schlüssel übergeben. Der Schlüssel ist ein void-Zeiger, und der Datentyp, das Format und die Bedeutung werden von der Anwendung definiert und sind für das Schriftsystem nicht transparent.

Während der Schlüssel alles sein kann, erfordert [DirectWrite,](direct-write-portal.md) dass jeder Schlüssel beide ist:

-   Eindeutig für eine einzelne Schriftartauflistung innerhalb des Ladeprogrammbereichs.
-   Gültig, bis die Registrierung des Ladeprogramm mithilfe der Factory aufgehoben wird.

Wenn die [**CreateCustomFontCollection-Methode**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createcustomfontcollection) aufgerufen wird, [ruft DirectWrite](direct-write-portal.md) eine [**IDWriteFontCollectionLoader-Schnittstelle**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollectionloader) zurück, die von der Anwendung als Singletonobjekt implementiert wird. Die [**Rückrufmethode IDWriteFontCollectionLoader::CreateEnumeratorFromKey**](/windows/win32/api/dwrite/nf-dwrite-idwritefontcollectionloader-createenumeratorfromkey) wird von DirectWrite verwendet, um ein von der Anwendung [**implementiertes IDWriteFontFileEnumerator-Objekt**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileenumerator) abzurufen. Das [**IDWriteFactory-Objekt,**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) das zum Erstellen der Auflistung verwendet wird, wird an diese Methode übergeben und sollte vom Schriftartdatei-Enumerator verwendet werden, um die [**IDWriteFontFile-Objekte**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile) zu erstellen, die in die Auflistung eingeschlossen werden sollen.

Der an diese Methode übergebene Schlüssel identifiziert die Schriftartauflistung und ist derselbe Schlüssel, der an [**CreateCustomFontCollection**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createcustomfontcollection)übergeben wird.

## <a name="idwritefontfileenumerator"></a>IDWriteFontFileEnumerator

Das anwendungsdefinierte [**IDWriteFontFileEnumerator-Objekt,**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileenumerator) das von der [**CreateEnumeratorFromKey-Methode**](/windows/win32/api/dwrite/nf-dwrite-idwritefontcollectionloader-createenumeratorfromkey) erstellt wurde, wird verwendet, um die Schriftartdateien in einer Auflistung aufzuzählen und ein [**IDWriteFontFile-Objekt**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile) für jede Datei zu erstellen. Die [**IDWriteFontFileEnumerator::MoveNext-Methode**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfileenumerator-movenext) ändert die Position in die nächste Schriftartdatei. Wenn eine Datei an der Position vorhanden ist, wird *hasCurrentFile* auf **TRUE** festgelegt. Andernfalls wird sie auf **FALSE** festgelegt, und die -Methode gibt **S \_ OK** zurück.

> [!Note]  
> Der Schriftartdatei-Enumerator muss vor dem ersten Element positioniert und beim ersten Aufruf von [**MoveNext**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfileenumerator-movenext)erweitert werden.

 

Ein [**IDWriteFontFile-Objekt**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile) wird von der [**IDWriteFontFileEnumerator::GetCurrentFontFile-Methode**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfileenumerator-getcurrentfontfile) ausgegeben. Wenn an der aktuellen Position keine Schriftartdatei vorhanden ist, da [**MoveNext**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfileenumerator-movenext) noch nicht aufgerufen wurde oder hasCurrentFile auf **FALSE** festgelegt wurde, gibt **GetCurrentFontFile** **E \_ FAIL** zurück.

## <a name="createcustomfontfilereference"></a>CreateCustomFontFileReference

Die [**IDWriteFontFile-Objektausgabe**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile) von [**GetCurrentFontFile**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfileenumerator-getcurrentfontfile) kann durch Aufrufen von [**IDWriteFactory::CreateCustomFontFileReference**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createcustomfontfilereference)erstellt werden. Der Verweisschlüssel für die Schriftartdatei identifiziert einen bestimmten Schriftartdateiverweis und muss innerhalb des Schriftartdateiladeprogramm, das die Datei lädt, eindeutig sein.

## <a name="idwritefontfileloader"></a>IDWriteFontFileLoader

Die [**CreateCustomFontFileReference-Methode**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createcustomfontfilereference) verwendet ein [**IDWriteFontFileLoader-Objekt,**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileloader) das von der Anwendung implementiert wird, die zum Laden der Schriftart verwendet wird. Die [**Rückrufmethode IDWriteFontFileLoader::CreateStreamFromKey**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfileloader-createstreamfromkey) wird an den Schlüssel übergeben und gibt ein [**IDWriteFontFileStream-Objekt**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfilestream) aus.

## <a name="idwritefontfilestream"></a>IDWriteFontFileStream

Das von der Anwendung [**implementierte IDWriteFontFileStream-Objekt**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfilestream) stellt die Schriftartdateidaten für einen Schriftartdateiverweis aus einem benutzerdefinierten Schriftartdateiladeprogramm bereit. Zusammen mit der Dateigröße und der letzten Schreibzeit stellt sie eine Methode ([**ReadFileFragment**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfilestream-readfilefragment)) zum Abrufen von Dateifragmenten bereit, die in ein [**IDWriteFontFile-Objekt**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile) kompiliert werden sollen.

> [!Note]  
> [**ReadFileFragment-Implementierungen**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfilestream-readfilefragment) sollten einen Fehler zurückgeben, wenn das angeforderte Fragment außerhalb der Dateigrenzen liegt.

 

Ein [**IDWriteFontFileStream**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfilestream) kann den Inhalt der Schriftartdatei von einem beliebigen Ort abrufen, z. B. von der lokalen Festplatte oder eingebetteten Ressourcen.

 

 