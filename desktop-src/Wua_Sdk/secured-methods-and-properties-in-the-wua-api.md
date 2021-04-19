---
description: Wenn WUA erkennt, dass ein Aufrufer nicht über die Berechtigung für den Zugriff auf eine Schnittstelle, Methode oder Eigenschaft verfügt, wird das HRESULT E \_ AccessDenied zurückgegeben.
ms.assetid: 4535ce8d-c329-4335-8b0a-8f63c22f111d
title: Sichern von Schnittstellen, Methoden und Eigenschaften in der WUA-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6680f616e1ca0596aba04edf4f7ddf7615e0c7f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106372845"
---
# <a name="securing-interfaces-methods-and-properties-in-the-wua-api"></a>Sichern von Schnittstellen, Methoden und Eigenschaften in der WUA-API

Einige Schnittstellen, Methoden und Eigenschaften von Windows Update-Agent (WUA) sind nur für Aufrufer zugänglich, die zu den folgenden Windows-Sicherheitsgruppen gehören:

-   Administrator
-   Benutzer
-   Poweruser

Wenn WUA erkennt, dass ein Aufrufer nicht über die Berechtigung für den Zugriff auf eine Schnittstelle, Methode oder Eigenschaft verfügt, wird das **HRESULT** E \_ AccessDenied zurückgegeben.

Die folgenden Schnittstellen sind für die Sicherheitsgruppen "Administrator", "Benutzer" und "Hauptbenutzer" verfügbar:

-   [**Iautomaticupdates**](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdates)
-   [**Iautomaticupdatessettings**](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdatessettings)
-   [**IAutomaticUpdatesSettings2**](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdatessettings2)
-   [**Isysteminformation**](/windows/desktop/api/Wuapi/nn-wuapi-isysteminformation)
-   [**Iupdatesearcher**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesearcher)
-   [**Iupdatesession**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession) und [ **IUpdateSession2**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession2)

> [!Note]  
> Wenn die folgenden Bedingungen zutreffen, schlägt die Suche fehl:
>
> -   Ein Benutzer, der kein Administrator ist, legt die [**UserLocale-Eigenschaft der IUpdateSession2**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesession2-get_userlocale) -Schnittstelle auf ein Gebiets Schema fest, das einer Sprache entspricht, die nicht auf dem Computer installiert ist.
> -   Bei der Suche wird ein updatesearch-Objekt verwendet, das aus dem updatesession-Objekt erstellt wurde.

 

Die folgenden Download Schnittstellen und-Methoden sind für die Administratoren und die Hauptbenutzer Gruppen verfügbar:

-   [**Iupdatedownloader**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatedownloader)
-   [**Iupdate:: copyfromcache**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-copyfromcache)
-   [**IAutomaticUpdatesSettings2:: checkberechtigung**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings2-checkpermission)
    > [!Note]  
    > Administratoren, Benutzer und Hauptbenutzer können [**IAutomaticUpdatesSettings2:: checkberechtigung**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings2-checkpermission)anrufen.

     

Die folgenden Installations Schnittstellen,-Methoden und-Eigenschaften sind für die Administrator Gruppen verfügbar:

-   [**Iautomaticupdates::P ause**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdates-pause)
-   [**Iautomaticupdates:: Resume**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdates-resume)
-   [**Iautomaticupdates:: enableservice**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdates-enableservice)
-   [**Iupdateingestaller**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateinstaller)
-   [**IsHidden-Eigenschaft von iupdate**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_ishidden)
    > [!Note]  
    > Administratoren, Benutzer und Hauptbenutzer können die Werte der [**IsHidden-Eigenschaft von iupdate**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_ishidden)abrufen. Allerdings können die Werte nur von Administratoren und Haupt Benutzern festgelegt werden.

     

-   [**Iupdate:: akzepteula**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-accepteula)
    > [!Note]  
    > Administratoren und Hauptbenutzer können die [**Methode "akzepteula" von iupdate**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-accepteula)aufzurufen.

     

-   [**Iautomaticupdatessettings:: Save**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-save)
-   [**NotificationLevel-Eigenschaft von iautomaticupdatessettings**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_notificationlevel)
    > [!Note]  
    > Administratoren, Benutzer und Hauptbenutzer können die Werte der [**notificationLevel-Eigenschaft von iautomaticupdatessettings**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_notificationlevel)abrufen. Die Werte können jedoch nur von Administratoren festgelegt werden.

     

-   [**Scheduledinstallationday-Eigenschaft von iautomaticupdatessettings**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationday)
    > [!Note]  
    > Administratoren, Benutzer und Hauptbenutzer können die Werte der [**Eigenschaft scheduledinstallationday von iautomaticupdatessettings**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationday)abrufen. Die Werte können jedoch nur von Administratoren festgelegt werden.

     

-   [**Scheduledinstallationtime-Eigenschaft von iautomaticupdatessettings**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationtime)
    > [!Note]  
    > Administratoren, Benutzer und Hauptbenutzer können die Werte der [**scheduledinstallationtime-Eigenschaft von iautomaticupdatessettings**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationtime)abrufen. Die Werte können jedoch nur von Administratoren festgelegt werden.

     

-   [**Includerecommendedupdates-Eigenschaft von IAutomaticUpdatesSettings2**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings2-get_includerecommendedupdates)
    > [!Note]  
    > Administratoren, Benutzer und Hauptbenutzer können die Werte der [**includerecommendedupdates-Eigenschaft von IAutomaticUpdatesSettings2**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings2-get_includerecommendedupdates)abrufen. Die Werte können jedoch nur von Administratoren festgelegt werden.

     

 

 



