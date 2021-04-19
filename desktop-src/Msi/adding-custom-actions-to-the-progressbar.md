---
description: Benutzerdefinierte Aktionen können einem ProgressBar-Steuerelement Zeit-und Fortschrittsinformationen hinzufügen. Weitere Informationen zum Erstellen eines Aktions Anzeige Dialogfelds mit einer ProgressBar finden Sie unter Erstellen eines ProgressBar-Steuer Elements.
ms.assetid: 101e6b59-3791-450c-9dc6-8930bd665a93
title: Hinzufügen von benutzerdefinierten Aktionen zur ProgressBar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ff2b6da9e72a37329b26cfce7590bab5f9792db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347964"
---
# <a name="adding-custom-actions-to-the-progressbar"></a>Hinzufügen von benutzerdefinierten Aktionen zur ProgressBar

[Benutzerdefinierte Aktionen](custom-actions.md) können einem [ProgressBar](progressbar-control.md) -Steuerelement Zeit-und Fortschrittsinformationen hinzufügen. Weitere Informationen zum Erstellen eines Aktions Anzeige Dialogfelds mit einer ProgressBar finden Sie unter [Erstellen eines ProgressBar-Steuer](authoring-a-progressbar-control.md)Elements.

Beachten Sie, dass dem Windows Installer Paket zwei benutzerdefinierte Aktionen hinzugefügt werden müssen, um Zeit-und Fortschrittsinformationen genau an die ProgressBar zu melden. Eine benutzerdefinierte Aktion muss eine verzögerte benutzerdefinierte Aktion sein. Diese benutzerdefinierte Aktion sollte die benutzerdefinierte Installation vervollständigen und die Beträge einzelner Inkremente an das [ProgressBar](progressbar-control.md) -Steuerelement senden, wenn das Installationsskript vom Installationsprogramm ausgeführt wird. Die zweite benutzerdefinierte Aktion muss eine benutzerdefinierte Aktion der unmittelbaren Ausführung sein, die der ProgressBar mitteilt, wie viele Ticks bei der Erfassungs-und Skript Generierungs Phase der Installation der Gesamtanzahl hinzugefügt werden sollen.

**So fügen Sie der ProgressBar eine benutzerdefinierte Aktion hinzu**

1.  Entscheiden Sie, wie der Fortschritt von der benutzerdefinierten Aktion beschrieben wird. Beispielsweise könnte eine benutzerdefinierte Aktion, die Registrierungsschlüssel installiert, eine Fortschrittsmeldung anzeigen und die [ProgressBar](progressbar-control.md) jedes Mal aktualisieren, wenn der Installer einen Registrierungsschlüssel schreibt.
2.  Jedes Update durch die benutzerdefinierte Aktion ändert die Länge der [ProgressBar](progressbar-control.md) durch ein konstantes Inkrement. Geben Sie die Anzahl der Ticks in jedem Inkrement an, oder berechnen Sie Sie. In der Regel entspricht eine Änderung der ProgressBar-Länge eines Tick der Installation von einem Byte. Wenn das Installationsprogramm z. b. ungefähr 10000 Byte beim Schreiben eines Registrierungsschlüssels installiert, können Sie angeben, dass in einem Inkrement 10000 Ticks vorhanden sind.
3.  Geben Sie die Gesamtzahl der Ticks an, die die benutzerdefinierte Aktion der Länge der [ProgressBar](progressbar-control.md)hinzufügt, oder berechnen Sie Sie. Die Anzahl der von der benutzerdefinierten Aktion hinzugefügten Ticks wird in der Regel wie folgt berechnet: (Tick Increment) x (Anzahl der Elemente). Wenn die benutzerdefinierte Aktion z. b. 10 Registrierungsschlüssel schreibt, installiert der Installer ungefähr 100000 bytes, und das Installationsprogramm muss daher die Schätzung der endgültigen Gesamtlänge der ProgressBar um 100000 Ticks erhöhen.
    > [!Note]  
    > Um dies dynamisch zu berechnen, muss die benutzerdefinierte Aktion einen Abschnitt enthalten, der sofort während der Skript Generierung ausgeführt wird. Die Menge der Ticks, die von der benutzerdefinierten Aktion der verzögerten Ausführung gemeldet wird, muss mit der Anzahl der Ticks übereinstimmen, die durch die sofortige Ausführungs Aktion der Gesamtzahl der Ticks hinzugefügt wird Wenn dies nicht der Fall ist, ist die vom timeremainung-Text Steuerelement gemeldete Zeit ungenau.

     

4.  Trennen Sie Ihre benutzerdefinierte Aktion in zwei Code Abschnitte: einen Abschnitt, der während der Skript Generierungs Phase ausgeführt wird, und einen Abschnitt, der während der Ausführungsphase der Installation ausgeführt wird. Hierfür können Sie zwei Dateien verwenden, oder Sie können eine Datei verwenden, indem Sie im Ausführ Modus des Installers eine Anlage ausführen. Im folgenden Beispiel wird eine Datei verwendet, und der Installationsstatus wird überprüft. Die Abschnitte des Beispiels sind abhängig davon, ob sich das Installationsprogramm in der Ausführungs-oder Skript Generierungs Phase der Installation befindet, abhängig davon, ob es ausgeführt wird.
5.  Der Abschnitt, der während der Erstellung des Skripts ausgeführt wird, sollte die Schätzung der endgültigen Gesamtlänge der [ProgressBar](progressbar-control.md) durch die Gesamtzahl der Ticks in der benutzerdefinierten Aktion erhöhen. Dies erfolgt durch Senden einer Statusmeldung " **progressaddition** ".
6.  Der Abschnitt, der in der Ausführungsphase der Installation ausgeführt wird, sollte Meldungs Text und Vorlagen einrichten, um den Benutzer darüber zu informieren, was die benutzerdefinierte Aktion ausführt, und den Installer beim Aktualisieren des [ProgressBar](progressbar-control.md) -Steuer Elements weiterzuleiten. Informieren Sie den Installer beispielsweise darüber, dass die ProgressBar ein Inkrement vorwärts bewegt wird, und senden Sie mit jedem Update eine explizite Statusmeldung. In diesem Abschnitt gibt es in der Regel eine Schleife, wenn die benutzerdefinierte Aktion etwas installiert. Bei jedem Durchlauf dieser Schleife kann das Installationsprogramm ein Verweis Element, z. b. einen Registrierungsschlüssel, installieren und das ProgressBar-Steuerelement aktualisieren.
7.  Fügen Sie Ihrem Windows Installer Paket eine benutzerdefinierte Aktion für die sofortige Ausführung hinzu. Durch diese benutzerdefinierte Aktion wird der [ProgressBar](progressbar-control.md) mitgeteilt, wie viel im Rahmen der Erfassungs-und Skript Generierungs Phasen der Installation fortzufahren ist. Im folgenden Beispiel ist die Quelle die dll, die durch Kompilieren des Beispielcodes erstellt wird, und das Ziel ist der Einstiegspunkt, caprogress.
8.  Fügen Sie Ihrem Windows Installer Paket eine benutzerdefinierte Aktion für die verzögerte Ausführung hinzu. Durch diese benutzerdefinierte Aktion werden die Schritte der eigentlichen Installation abgeschlossen und der [ProgressBar](progressbar-control.md) mitgeteilt, wie viel Zeit für die Ausführung des Installations Skripts durch das Installationsprogramm erforderlich ist. Im folgenden Beispiel ist die Quelle die dll, die durch Kompilieren des Beispielcodes erstellt wird, und das Ziel ist der Einstiegspunkt, caprogress.
9.  Planen Sie sowohl benutzerdefinierte Aktionen zwischen [InstallInitialize](installinitialize-action.md) und [InstallFinalize](installfinalize-action.md) in der [InstallExecuteSequence](installexecutesequence-table.md) -Tabelle. Die verzögerte benutzerdefinierte Aktion sollte unmittelbar nach der benutzerdefinierten Aktion "sofortige Ausführung" geplant werden. Der Installer führt die verzögerte benutzerdefinierte Aktion erst aus, nachdem das Skript ausgeführt wurde.

Im folgenden Beispiel wird gezeigt, wie der [ProgressBar](progressbar-control.md)eine benutzerdefinierte Aktion hinzugefügt werden kann. Die Quelle der beiden benutzerdefinierten Aktionen ist die dll, die durch Kompilieren des Beispielcodes erstellt wird, und das Ziel der beiden benutzerdefinierten Aktionen ist der Einstiegspunkt, caprogress. In diesem Beispiel werden keine tatsächlichen Änderungen am System vorgenommen, sondern die ProgressBar so betrieben, als ob 10 Verweis Elemente mit einer Größe von ungefähr 10.000 Byte installiert werden. Das Installationsprogramm aktualisiert die Meldung und die ProgressBar bei jeder Installation eines Verweis Elements.


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



 

 



