---
title: Automatisierte Sperrung und Erneuerung von Komponenten
description: Automatisierte Sperrung und Erneuerung von Komponenten
ms.assetid: be4899d7-1d87-4450-8c0e-75cf112ca66a
keywords:
- Windows Media-Format-SDK, automatisierte Sperrung und Verlängerung
- Windows Media-Format-SDK, Widerruf
- SDK für Windows Media-Format, Erneuerung
- Digital Rights Management (DRM), automatisierte Sperrung und Erneuerung
- DRM (Digital Rights Management), automatisierte Sperrung und Erneuerung
- Digital Rights Management (DRM), Sperrung
- DRM (Digital Rights Management), Sperrung
- Digital Rights Management (DRM), Erneuerung
- DRM (Digital Rights Management), Erneuerung
- Erweiterte APIs für den DRM-Client, automatisierte Sperrung und Verlängerung
- Erweiterte Client-APIs, automatisierte Sperrung und Verlängerung
- Erweiterte APIs für den DRM-Client, Sperrung
- Erweiterte Client-APIs, Sperrung
- Erweiterte APIs für den DRM-Client, Erneuerung
- Erweiterte Client-APIs, Erneuerung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b9046d04d8ca7a138a06cba4d26cd82bc5a12b2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315999"
---
# <a name="automated-component-revocation-and-renewal"></a>Automatisierte Sperrung und Erneuerung von Komponenten

Software Anwendungen oder Komponenten, die als kompromittiert angesehen werden, können von Microsoft widerrufen werden. Die erweiterte API des Windows Media-Format Clients bietet einen Mechanismus für die automatisierte Sperrung und Erneuerung von-Komponenten.

Widerrufene Komponenten werden in einer Zertifikat Sperr Liste aufgelistet, die von Microsoft veröffentlicht wird. Wenn eine Komponente widerrufen wird, wird Ihr Zertifikat der Zertifikat Sperr Liste hinzugefügt, und das Sperr Informations-BLOB (Rev \_ Info) wird auf den Microsoft-Servern aktualisiert.

Zum automatischen Sperren und erneuern, wenn ein Benutzer versucht, von Windows Media DRM geschützte Inhalte zu verarbeiten, muss Ihre Anwendung folgende Aktionen ausführen:

1.  Extrahieren Sie die Rev \_ Info-Version aus der Lizenz. Die Versionsnummer der Rev- \_ Info befindet sich an folgendem Speicherort in einer XMR-Lizenz:
    ```C++
    <LICENSE version="2.0.0.0">
        <LICENSORINFO/>
        <DATA>
            <LID>...</LID>
            <KID>...</KID>
            <RevInfoVersion>42</RevInfoVersion>
            ...
         </DATA>
    ....
    </LICENSE>
    ```

    

2.  Vergleichen Sie die \_ Versionsnummer der Rev-Info der Lizenz mit der Versionsnummer der Rev- \_ Info im lokalen Speicher, indem Sie die [**iwmdrmsecurity:: getrevocationdataversion**](iwmdrmsecurity-getrevocationdataversion.md) -Methode aufrufen.
3.  Wenn die Rev \_ Info-Version nicht auf dem neuesten Stand ist, rufen Sie die [**iwmdrmsecurity::P erformsecurityupdate**](iwmdrmsecurity-performsecurityupdate.md) -Methode auf, und übergeben Sie \_ \_ \_ \_ im *dwFlags* -Parameter das Flag für die WMDRM-Sicherheits Ausführung-Sperr Aktualisierung.
4.  Rufen Sie die Zertifikat Sperr Liste aus dem lokalen Speicher ab, indem Sie die [**iwmdrmsecurity:: getrevocationdata**](iwmdrmsecurity-getrevocationdata.md) -Methode aufrufen.
5.  Analysieren Sie die Sperr Liste, und überprüfen Sie, ob Windows Media DRM-Widerrufungen angezeigt werden. Weitere Informationen finden Sie unter über [Prüfen der Zertifikat](checking-certificate-revocation.md)Sperrung.
6.  Wenn Windows Media DRM-widerrufen vorhanden sind:
    1.  Erstellen Sie einen Inhalts-Wegbereiter zum Erneuern der gesperrten Komponenten, indem Sie die [**iwmdrmsecurity:: getcontentenablersforrevocations**](iwmdrmsecurity-getcontentenablersforrevocations.md) -Methode aufrufen.
    2.  Der Aufruf von **imfcontentenabler:: automaticenable** leitet den Benutzer an eine URL weiter, die Informationen zur Erneuerung der Komponente enthält. Diese Methode wird im [Media Foundation SDK](../medfound/microsoft-media-foundation-sdk.md) () dokumentiert https://msdn.microsoft.com/library/ms694197(VS.85).aspx) .
        > [!Note]  
        > Sie müssen diesen Prozess für den Benutzer durch die Verwendung einer Datenschutzerklärung verdeutlichen, da der Aktualisierungsprozess Informationen vom Client Computer an eine Microsoft-Website sendet.

         

    3.  Wenn möglich, erneuert der Benutzer die Komponente über die URL, entweder automatisch oder durch Befolgen bestimmter Anweisungen. Es gibt Situationen, in denen die Komponente nicht erneuert werden kann.
    4.  Versuchen Sie erneut, auf den Inhalt zuzugreifen, bis keine weiteren widerrufen vorhanden sind oder der Prozess aus irgendeinem Grund angehalten wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Programmierhandbuch**](drm-programming-guide.md)
</dt> </dl>

 

 