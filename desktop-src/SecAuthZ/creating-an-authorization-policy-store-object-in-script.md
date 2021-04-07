---
description: Ein Autorisierungs Richtlinien Speicher enthält Informationen über die Sicherheitsrichtlinie einer Anwendung oder Gruppe von Anwendungen.
ms.assetid: bce85da8-11de-4bc1-b097-d8efdbd28abf
title: Erstellen eines Autorisierungs Richtlinien-Speicher Objekts im Skript
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: feb02c80408210b663524e2aa914852a853e80ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863248"
---
# <a name="creating-an-authorization-policy-store-object-in-script"></a>Erstellen eines Autorisierungs Richtlinien-Speicher Objekts im Skript

Ein Autorisierungs Richtlinien Speicher enthält Informationen über die Sicherheitsrichtlinie einer Anwendung oder Gruppe von Anwendungen. Zu diesen Informationen gehören die Anwendungen, Vorgänge, Tasks, Benutzer und Gruppen von Benutzern, die dem Speicher zugeordnet sind. Wenn eine Anwendung, die den Autorisierungs-Manager verwendet, initialisiert, lädt Sie diese Informationen aus dem Speicher. Der Autorisierungs Richtlinien Speicher muss sich in einem vertrauenswürdigen System befinden, da Administratoren auf diesem System über ein hohes Maß an Zugriff auf den Store verfügen.

Der Autorisierungs-Manager unterstützt das Speichern von Autorisierungs Richtlinien entweder im Active Directory Directory-Dienst oder in einer XML-Datei, wie in den folgenden Beispielen gezeigt. In der Autorisierungs-Manager-API wird ein Autorisierungs Richtlinien Speicher durch ein [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) -Objekt dargestellt. In den Beispielen wird gezeigt, wie ein **AzAuthorizationStore** -Objekt für einen Active Directory-Speicher und einen XML-Speicher erstellt wird.

-   [Erstellen eines Active Directory Stores](#creating-an-active-directory-store)
-   [Erstellen eines SQL Server Stores](#creating-a-sql-server-store)
-   [Erstellen eines XML-Stores](#creating-an-xml-store)

## <a name="creating-an-active-directory-store"></a>Erstellen eines Active Directory Stores

Um Active Directory zum Speichern der Autorisierungs Richtlinie zu verwenden, muss sich die Domäne auf der **Windows Server 2003** -Domänen Funktionsebene befinden. Der Autorisierungs Richtlinien Speicher kann nicht in einem **nicht-Domänen-namens Kontext** (auch als Anwendungs Partition bezeichnet) gefunden werden. Es wird empfohlen, dass sich der Speicher im **Programm Daten** Container unter einer neuen Organisationseinheit befindet, die speziell für den Autorisierungs Richtlinien Speicher erstellt wurde. Außerdem wird empfohlen, dass sich der Speicher innerhalb desselben lokalen Netzwerks befindet wie Anwendungsserver, die Anwendungen ausführen, die den Speicher verwenden.

Im folgenden Beispiel wird gezeigt, wie ein [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) -Objekt erstellt wird, das einen Autorisierungs Richtlinien Speicher in Active Directory darstellt. In diesem Beispiel wird davon ausgegangen, dass in einer Domäne mit dem Namen AuthManager.com eine vorhandene Organisationseinheit mit dem Namen Program Data Active Directory vorhanden ist.


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



## <a name="creating-a-sql-server-store"></a>Erstellen eines SQL Server Stores

Der Autorisierungs-Manager unterstützt das Erstellen eines Microsoft SQL Server – basierten Autorisierungs Richtlinien Speicher. Um einen SQL Server – basierten Autorisierungs Speicher zu erstellen, verwenden Sie eine URL, die mit dem Präfix **MSSQL://** beginnt. Die URL muss eine gültige SQL-Verbindungs Zeichenfolge, einen Datenbanknamen und den Namen des Autorisierungs Richtlinien Speicher enthalten: **MSSQL://**_ConnectionString_ *_/_* _DatabaseName_ *_/_* _policystorename_.

Wenn die Instanz von SQL Server die angegebene Autorisierungs-Manager-Datenbank nicht enthält, erstellt der Autorisierungs-Manager eine neue Datenbank mit diesem Namen.

> [!Note]  
> Verbindungen mit einem SQL Server Speicher werden nur dann verschlüsselt, wenn Sie die SQL-Verschlüsselung für die Verbindung explizit einrichten oder die Verschlüsselung des Netzwerk Datenverkehrs einrichten, der IPSec (Internet Protocol Security) verwendet.

 

Im folgenden Beispiel wird gezeigt, wie ein [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) -Objekt erstellt wird, das einen Autorisierungs Richtlinien Speicher in einer SQL Server-Datenbank darstellt.


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



## <a name="creating-an-xml-store"></a>Erstellen eines XML-Stores

Der Autorisierungs-Manager unterstützt das Erstellen eines Autorisierungs Richtlinien Speicher im XML-Format Der XML-Speicher kann sich auf demselben Computer befinden, auf dem die Anwendung ausgeführt wird, oder er kann Remote gespeichert werden. Das direkte Bearbeiten der XML-Datei wird nicht unterstützt. Verwenden Sie das Autorisierungs-Manager-MMC-Snap-in oder die Autorisierungs-Manager-API zum Bearbeiten des Richtlinien Speicher.

Der Autorisierungs-Manager unterstützt nicht die Delegierung der Verwaltung eines XML-Richtlinien Speicher. Weitere Informationen zur Delegierung finden Sie unter [Delegieren der Definition von Berechtigungen in Skripts](delegating-the-defining-of-permissions-in-script.md).

Im folgenden Beispiel wird gezeigt, wie ein [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) -Objekt erstellt wird, das einen Autorisierungs Richtlinien Speicher in einer XML-Datei darstellt.


```VB
'  Create the store object.
Dim authStore
Set authStore = CreateObject("AzRoles.AzAuthorizationStore")

'  Initialize the store object.
authStore.Initialize 1, "msxml://C:\MyStore.xml"

'  Save information to the store.
authStore.Submit
```



 

 



