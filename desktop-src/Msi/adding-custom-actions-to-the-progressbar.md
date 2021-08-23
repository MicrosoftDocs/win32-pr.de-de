---
description: Benutzerdefinierte Aktionen können einem ProgressBar-Steuerelement Zeit- und Fortschrittsinformationen hinzufügen. Weitere Informationen zum Erstellen eines Aktionsanzeigedialogfelds mit einer ProgressBar finden Sie unter Erstellen eines ProgressBar-Steuerelements.
ms.assetid: 101e6b59-3791-450c-9dc6-8930bd665a93
title: Hinzufügen benutzerdefinierter Aktionen zur ProgressBar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d83dfeb806eb0ed6f1e251dd48b97911d8e0f583c8b65cb48ef0d04df059ebb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119811060"
---
# <a name="adding-custom-actions-to-the-progressbar"></a>Hinzufügen benutzerdefinierter Aktionen zur ProgressBar

[Benutzerdefinierte Aktionen](custom-actions.md) können einem ProgressBar-Steuerelement Zeit- und [Fortschrittsinformationen](progressbar-control.md) hinzufügen. Weitere Informationen zum Erstellen eines Aktionsanzeigedialogfelds mit einer ProgressBar finden Sie unter [Erstellen eines ProgressBar-Steuerelements.](authoring-a-progressbar-control.md)

Beachten Sie, dass zwei benutzerdefinierte Aktionen zum Paket Windows Installer hinzugefügt werden müssen, um Zeit- und Fortschrittsinformationen korrekt an die ProgressBar zu melden. Eine benutzerdefinierte Aktion muss eine verzögerte benutzerdefinierte Aktion sein. Diese benutzerdefinierte Aktion sollte ihre benutzerdefinierte Installation abschließen und die Mengen einzelner Inkremente an das [ProgressBar-Steuerelement](progressbar-control.md) senden, wenn das Installationsprogramm das Installationsskript ausgeführt. Bei der zweiten benutzerdefinierten Aktion muss es sich um eine benutzerdefinierte Aktion zur sofortigen Ausführung handeln, die progressBar darüber informiert, wie viele Ticks der Gesamtzahl während der Erfassungs- und Skriptgenerierungsphase der Installation hinzugefügt werden sollen.

**So fügen Sie der ProgressBar eine benutzerdefinierte Aktion hinzu**

1.  Entscheiden Sie, wie der Fortschritt der benutzerdefinierten Aktion beschrieben wird. Beispielsweise könnte eine benutzerdefinierte Aktion, die Registrierungsschlüssel installiert, eine Statusmeldung anzeigen und [die ProgressBar](progressbar-control.md) jedes Mal aktualisieren, wenn das Installationsprogramm einen Registrierungsschlüssel schreibt.
2.  Jedes Update durch die benutzerdefinierte Aktion ändert die Länge der [ProgressBar](progressbar-control.md) um ein konstantes Inkrement. Geben Sie die Anzahl der Ticks in jedem Inkrement an, oder berechnen Sie sie. In der Regel entspricht eine Änderung der ProgressBar-Länge eines Ticks der Installation eines Byte. Wenn das Installationsprogramm beispielsweise ungefähr 1.000 Byte installiert, wenn es einen Registrierungsschlüssel schreibt, können Sie angeben, dass in einem Inkrement 1.0000 Ticks vorhanden sind.
3.  Geben Sie die Gesamtanzahl von Teilstrichen an, die die benutzerdefinierte Aktion zur Länge der ProgressBar hinzufügt, oder berechnen [Sie sie.](progressbar-control.md) Die Anzahl von Ticks, die von der benutzerdefinierten Aktion hinzugefügt werden, wird in der Regel wie folgt berechnet: (Teilstrichinkrement) x (Anzahl von Elementen). Wenn die benutzerdefinierte Aktion beispielsweise 10 Registrierungsschlüssel schreibt, installiert das Installationsprogramm ungefähr 100.000 Byte, und das Installationsprogramm muss daher die Schätzung der endgültigen Gesamtlänge der ProgressBar um 100.000 Ticks erhöhen.
    > [!Note]  
    > Um dies dynamisch zu berechnen, muss die benutzerdefinierte Aktion einen Abschnitt enthalten, der sofort während der Skriptgenerierung ausgeführt wird. Die Anzahl der Ticks, die von Ihrer benutzerdefinierten Aktion für die verzögerte Ausführung gemeldet werden, muss der Anzahl von Ticks entspricht, die der Gesamtzahl der Ticks durch die sofortige Ausführungsaktion hinzugefügt wurden. Wenn dies nicht der Fall ist, ist die vom TimeRemaining-Textsteuerfeld gemeldete Zeit ungenau.

     

4.  Trennen Sie Ihre benutzerdefinierte Aktion in zwei Codeabschnitte: einen Abschnitt, der während der Skriptgenerierungsphase ausgeführt wird, und einen Abschnitt, der während der Ausführungsphase der Installation ausgeführt wird. Sie können dazu zwei Dateien verwenden, oder Sie können eine Datei verwenden, indem Sie den Ausführungsmodus des Installationsprogramms verwenden. Im folgenden Beispiel wird eine Datei verwendet und der Installationsstatus überprüft. Abschnitte des Beispiels müssen abhängig davon ausgeführt werden, ob sich das Installationsprogramm in der Ausführungs- oder Skriptgenerierungsphase der Installation befindet.
5.  Der Abschnitt, der während der Skriptgenerierung ausgeführt wird, sollte die Schätzung der endgültigen Gesamtlänge der [ProgressBar](progressbar-control.md) um die Gesamtzahl der Ticks in der benutzerdefinierten Aktion erhöhen. Dies erfolgt durch Senden einer **ProgressAddition-Statusmeldung.**
6.  Der Abschnitt, der während der Ausführungsphase der Installation ausgeführt wird, sollte Meldungstext und Vorlagen einrichten, um den Benutzer über die Aktionen der benutzerdefinierten Aktion zu informieren und das Installationsprogramm beim Aktualisieren des [ProgressBar-Steuerelements zu](progressbar-control.md) informieren. Informieren Sie z. B. das Installationsprogramm, die ProgressBar um ein Inkrement nach vorn zu verschieben und bei jedem Update eine explizite Statusmeldung zu senden. In diesem Abschnitt gibt es in der Regel eine Schleife, wenn die benutzerdefinierte Aktion etwas installiert. Bei jedem Durchlauf dieser Schleife kann das Installationsprogramm ein Verweiselement installieren, z. B. einen Registrierungsschlüssel, und das ProgressBar-Steuerelement aktualisieren.
7.  Fügen Sie eine benutzerdefinierte Aktion zur sofortigen Ausführung zu Ihrem Windows Installer-Paket hinzu. Diese benutzerdefinierte Aktion informiert [die ProgressBar](progressbar-control.md) darüber, wie viel während der Phasen "Erwerb" und "Skriptgenerierung" der Installation vorgefertigt werden soll. Im folgenden Beispiel ist die Quelle die DLL, die durch Kompilieren des Beispielcodes erstellt wurde, und das Ziel ist der Einstiegspunkt CAProgress.
8.  Fügen Sie eine benutzerdefinierte Aktion für die verzögerte Ausführung zu Ihrem Windows Installer-Paket hinzu. Diese benutzerdefinierte Aktion führt die Schritte der eigentlichen Installation aus und informiert [die ProgressBar](progressbar-control.md) darüber, wie viel die Leiste zum Zeitpunkt der Ausführung des Installationsskripts durch das Installationsprogramm vorankommen soll. Im folgenden Beispiel ist die Quelle die DLL, die durch Kompilieren des Beispielcodes erstellt wurde, und das Ziel ist der Einstiegspunkt CAProgress.
9.  Planen Sie in der Tabelle [InstallExecuteSequence](installexecutesequence-table.md) beide benutzerdefinierten Aktionen zwischen [InstallInitialize](installinitialize-action.md) und [InstallFinalize.](installfinalize-action.md) Die verzögerte benutzerdefinierte Aktion sollte unmittelbar nach der benutzerdefinierten Aktion für die sofortige Ausführung geplant werden. Das Installationsprogramm führt die verzögerte benutzerdefinierte Aktion erst aus, wenn das Skript ausgeführt wird.

Das folgende Beispiel zeigt, wie eine benutzerdefinierte Aktion der [ProgressBar hinzugefügt werden kann.](progressbar-control.md) Die Quelle beider benutzerdefinierter Aktionen ist die DLL, die durch Kompilieren des Beispielcodes erstellt wird, und das Ziel beider benutzerdefinierter Aktionen ist der Einstiegspunkt CAProgress. Dieses Beispiel nimmt keine tatsächlichen Änderungen am System vor, sondern führt die ProgressBar so aus, als ob 10 Referenzelemente installiert würden, die jeweils ungefähr 10.000 Byte groß sind. Das Installationsprogramm aktualisiert die Meldung und ProgressBar jedes Mal, wenn ein Verweiselement installiert wird.


```C++
#include <windows.h>
#include <msiquery.h>
#pragma comment(lib, "msi.lib")

// Specify or calculate the number of ticks in an increment
// to the ProgressBar
const UINT iTickIncrement = 10000;
 
// Specify or calculate the total number of ticks the custom 
// action adds to the length of the ProgressBar
const UINT iNumberItems = 10;
const UINT iTotalTicks = iTickIncrement * iNumberItems;
 
UINT __stdcall CAProgress(MSIHANDLE hInstall)
{
    // Tell the installer to check the installation state and execute
    // the code needed during the rollback, acquisition, or
    // execution phases of the installation.
  
    if (MsiGetMode(hInstall,MSIRUNMODE_SCHEDULED) == TRUE)
    {
        PMSIHANDLE hActionRec = MsiCreateRecord(3);
        PMSIHANDLE hProgressRec = MsiCreateRecord(3);

        // Installer is executing the installation script. Set up a
        // record specifying appropriate templates and text for
        // messages that will inform the user about what the custom
        // action is doing. Tell the installer to use this template and 
        // text in progress messages.
 
        MsiRecordSetString(hActionRec, 1, TEXT("MyCustomAction"));
        MsiRecordSetString(hActionRec, 2, TEXT("Incrementing the Progress Bar..."));
        MsiRecordSetString(hActionRec, 3, TEXT("Incrementing tick [1] of [2]"));
        UINT iResult = MsiProcessMessage(hInstall, INSTALLMESSAGE_ACTIONSTART, hActionRec);
        if ((iResult == IDCANCEL))
            return ERROR_INSTALL_USEREXIT;
              
        // Tell the installer to use explicit progress messages.
        MsiRecordSetInteger(hProgressRec, 1, 1);
        MsiRecordSetInteger(hProgressRec, 2, 1);
        MsiRecordSetInteger(hProgressRec, 3, 0);
        iResult = MsiProcessMessage(hInstall, INSTALLMESSAGE_PROGRESS, hProgressRec);
        if ((iResult == IDCANCEL))
            return ERROR_INSTALL_USEREXIT;
              
        //Specify that an update of the progress bar's position in
        //this case means to move it forward by one increment.
        MsiRecordSetInteger(hProgressRec, 1, 2);
        MsiRecordSetInteger(hProgressRec, 2, iTickIncrement);
        MsiRecordSetInteger(hProgressRec, 3, 0);
 
        // The following loop sets up the record needed by the action
        // messages and tells the installer to send a message to update
        // the progress bar.

        MsiRecordSetInteger(hActionRec, 2, iTotalTicks);
       
        for( int i = 0; i < iTotalTicks; i+=iTickIncrement)
        {
            MsiRecordSetInteger(hActionRec, 1, i);

            iResult = MsiProcessMessage(hInstall, INSTALLMESSAGE_ACTIONDATA, hActionRec);
            if ((iResult == IDCANCEL))
                return ERROR_INSTALL_USEREXIT;
          
            iResult = MsiProcessMessage(hInstall, INSTALLMESSAGE_PROGRESS, hProgressRec);
            if ((iResult == IDCANCEL))
                return ERROR_INSTALL_USEREXIT;
   
            //A real custom action would have code here that does a part
            //of the installation. For this sample, code that installs
            //10 registry keys.
            Sleep(1000);
                    
        }
        return ERROR_SUCCESS;
    }
    else
    {
        // Installer is generating the installation script of the
        // custom action.
  
        // Tell the installer to increase the value of the final total
        // length of the progress bar by the total number of ticks in
        // the custom action.
        PMSIHANDLE hProgressRec = MsiCreateRecord(2);

         MsiRecordSetInteger(hProgressRec, 1, 3);
            MsiRecordSetInteger(hProgressRec, 2, iTotalTicks);
        UINT iResult = MsiProcessMessage(hInstall, INSTALLMESSAGE_PROGRESS, hProgressRec);
           if ((iResult == IDCANCEL))
            return ERROR_INSTALL_USEREXIT;     
        return ERROR_SUCCESS;
     }
}
```



 

 



