---
description: Ein Autorisierungsrichtlinienspeicher enthält Informationen zur Sicherheitsrichtlinie einer Anwendung oder Gruppe von Anwendungen.
ms.assetid: bce85da8-11de-4bc1-b097-d8efdbd28abf
title: Erstellen einer Autorisierungsrichtlinie Store-Objekts im Skript
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 409a22df52d2914cd205700afccfc7a59f19031d924a921b5f2e5101621a895a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117782195"
---
# <a name="creating-an-authorization-policy-store-object-in-script"></a>Erstellen einer Autorisierungsrichtlinie Store-Objekts im Skript

Ein Autorisierungsrichtlinienspeicher enthält Informationen zur Sicherheitsrichtlinie einer Anwendung oder Gruppe von Anwendungen. Die Informationen umfassen die Anwendungen, Vorgänge, Aufgaben, Benutzer und Benutzergruppen, die dem Speicher zugeordnet sind. Wenn eine Anwendung, die den Autorisierungs-Manager verwendet, initialisiert wird, lädt sie diese Informationen aus dem Speicher. Der Autorisierungsrichtlinienspeicher muss sich auf einem vertrauenswürdigen System befinden, da Administratoren auf diesem System einen hohen Zugriff auf den Speicher haben.

Autorisierungs-Manager unterstützt das Speichern von Autorisierungsrichtlinien im Active Directory-Verzeichnisdienst oder in einer XML-Datei, wie in den folgenden Beispielen gezeigt. In der Autorisierungs-Manager-API wird ein Autorisierungsrichtlinienspeicher durch ein [**AzAuthorizationStore-Objekt**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) dargestellt. Die Beispiele zeigen, wie ein **AzAuthorizationStore-Objekt** für einen Active Directory-Speicher und einen XML-Speicher erstellt wird.

-   [Erstellen eines Active Directory-Store](#creating-an-active-directory-store)
-   [Erstellen eines SQL Server Store](#creating-a-sql-server-store)
-   [Erstellen eines XML-Store](#creating-an-xml-store)

## <a name="creating-an-active-directory-store"></a>Erstellen eines Active Directory-Store

Um Active Directory zum Speichern der Autorisierungsrichtlinie zu verwenden, muss sich die Domäne auf der **Domänenfunktionsebene Windows Server 2003** befinden. Der Autorisierungsrichtlinienspeicher kann sich nicht in einem **Nichtdomänenbenennungskontext** (auch als Anwendungspartition bezeichnet) befinden. Es wird empfohlen, dass sich der Speicher im **Container Programmdaten** in einer neuen Organisationseinheit befindet, die speziell für den Autorisierungsrichtlinienspeicher erstellt wurde. Es wird auch empfohlen, dass sich der Speicher im selben lokalen Netzwerk wie Anwendungsserver befindet, auf denen Anwendungen ausgeführt werden, die den Speicher verwenden.

Das folgende Beispiel zeigt, wie Sie ein [**AzAuthorizationStore-Objekt**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) erstellen, das einen Autorisierungsrichtlinienspeicher in Active Directory darstellt. Im Beispiel wird davon ausgegangen, dass eine vorhandene Active Directory-Organisationseinheit namens Program Data in einer Domäne mit dem Namen authmanager.com vorhanden ist.


```VB
'  Create the store object.
Dim authStore
Set authStore = CreateObject("AzRoles.AzAuthorizationStore")

'  Initialize the store object.
authStore.Initialize 1, _
    "msldap://CN=MyStore, CN=Program Data,DC=authmanager,DC=com"

'  Save the information to the store.
authStore.Submit
```



## <a name="creating-a-sql-server-store"></a>Erstellen eines SQL Server Store

Der Autorisierungs-Manager unterstützt das Erstellen eines Microsoft SQL Server basierten Autorisierungsrichtlinienspeichers. Um einen SQL Server basierten Autorisierungsspeicher zu erstellen, verwenden Sie eine URL, die mit dem Präfix **MSSQL://** beginnt. Die URL muss eine gültige SQL Verbindungszeichenfolge, einen Datenbanknamen und den Namen des Autorisierungsrichtlinienspeichers enthalten: **MSSQL://**_ConnectionString_ *_/_* _DatabaseName_ *_/_* _PolicyStoreName_.

Wenn die Instanz von SQL Server nicht die angegebene Autorisierungs-Manager-Datenbank enthält, erstellt der Autorisierungs-Manager eine neue Datenbank mit diesem Namen.

> [!Note]  
> Verbindungen mit einem SQL Server-Speicher werden nicht verschlüsselt, es sei denn, Sie richten explizit SQL Verschlüsselung für die Verbindung ein oder richten die Verschlüsselung des Netzwerkdatenverkehrs ein, der Internetprotokollsicherheit (Internet Protocol Security, IPsec) verwendet.

 

Das folgende Beispiel zeigt, wie Sie ein [**AzAuthorizationStore-Objekt**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) erstellen, das einen Autorisierungsrichtlinienspeicher in einer SQL Server Datenbank darstellt.


```VB
'  Create the store object.
Dim authStore
Set authStore = CreateObject("AzRoles.AzAuthorizationStore")

'  Initialize the store object.
authStore.Initialize 1, _ 
  "MSSQL://Driver={SQL Server};Server={AzServer};/AzDB/MyStore"

'  Save information to the store.
authStore.Submit
```



## <a name="creating-an-xml-store"></a>Erstellen eines XML-Store

Der Autorisierungs-Manager unterstützt das Erstellen eines Autorisierungsrichtlinienspeichers im XML-Format. Der XML-Speicher kann sich auf demselben Computer befinden, auf dem die Anwendung ausgeführt wird, oder er kann remote gespeichert werden. Das direkte Bearbeiten der XML-Datei wird nicht unterstützt. Verwenden Sie das MMC-Snap-In für den Autorisierungs-Manager oder die Autorisierungs-Manager-API, um den Richtlinienspeicher zu bearbeiten.

Der Autorisierungs-Manager unterstützt nicht das Delegieren der Verwaltung eines XML-Richtlinienspeichers. Informationen zur Delegierung finden Sie unter [Delegieren der Definition von Berechtigungen in Skript](delegating-the-defining-of-permissions-in-script.md).

Das folgende Beispiel zeigt, wie Sie ein [**AzAuthorizationStore-Objekt**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) erstellen, das einen Autorisierungsrichtlinienspeicher in einer XML-Datei darstellt.


```VB
'  Create the store object.
Dim authStore
Set authStore = CreateObject("AzRoles.AzAuthorizationStore")

'  Initialize the store object.
authStore.Initialize 1, "msxml://C:\MyStore.xml"

'  Save information to the store.
authStore.Submit
```



 

 



