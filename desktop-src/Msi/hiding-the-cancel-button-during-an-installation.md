---
description: Sie können die Schaltfläche Abbrechen ausblenden, die zum Abbrechen einer Installation verwendet wird, indem Sie eine Befehlszeilenoption, die Windows Installer-API oder eine benutzerdefinierte Aktion verwenden. Die Schaltfläche Abbrechen kann für einen Teil oder die gesamte Installation ausgeblendet werden, je nachdem, welche Methode Sie verwenden.
ms.assetid: de2bb788-0d19-4818-8038-cae6000b38c4
title: Ausblenden der Schaltfläche "Abbrechen" während einer Installation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9b838803b65b8923dc45f36e17579e30114c1bc6d86c8fba2e533252e524568
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129530"
---
# <a name="hiding-the-cancel-button-during-an-installation"></a>Ausblenden der Schaltfläche "Abbrechen" während einer Installation

Sie können die Schaltfläche **Abbrechen** ausblenden, die zum Abbrechen einer Installation verwendet wird, indem Sie eine Befehlszeilenoption, die Windows Installer-API oder eine benutzerdefinierte Aktion verwenden. Die Schaltfläche **Abbrechen** kann für einen Teil oder die gesamte Installation ausgeblendet werden, je nachdem, welche Methode Sie verwenden.

## <a name="hiding-the-cancel-button-from-the-command-line"></a>Ausblenden der Schaltfläche "Abbrechen" über die Befehlszeile

Die Schaltfläche **Abbrechen** kann während der Installation mithilfe der Befehlszeilenoption (!) ausgeblendet werden. Dies kann nur für eine einfache Installation auf Benutzeroberflächenebene (/qb) erfolgen. Die Schaltfläche **Abbrechen** ist für die gesamte Installation ausgeblendet. Weitere Informationen finden Sie unter [Befehlszeilenoptionen](command-line-options.md) und [Benutzeroberfläche Ebenen.](user-interface-levels.md) Die folgende Befehlszeile blendet die Schaltfläche **Abbrechen** aus und installiert Example.msi.

**msiexec /I example.msi /qb!**

## <a name="hiding-the-cancel-button-from-an-application-or-script"></a>Ausblenden der Schaltfläche "Abbrechen" aus einer Anwendung oder einem Skript

Sie können eine Anwendung oder ein Skript schreiben, um die Schaltfläche **Abbrechen** auszublenden. Dies kann nur für eine einfache Installation auf Benutzeroberflächenebene erfolgen, sodass die Schaltfläche **Abbrechen** für die gesamte Installation ausgeblendet wird.

Um die Schaltfläche Abbrechen in einer Anwendung auszublenden, legen Sie INSTALLUILEVEL \_ HIDECANCEL beim Aufrufen von [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui)fest. Im folgenden Beispiel wird die Schaltfläche **Abbrechen** ausgeblendet und Example.msi installiert.


```C++
#include <windows.h>
#include <stdio.h>
#include <Shellapi.h>
#include <msi.h>
#include <Msiquery.h>
#include <tchar.h>
#pragma comment(lib, "msi.lib")

int main()  
{

INSTALLUILEVEL uiPrevLevel = MsiSetInternalUI( INSTALLUILEVEL(INSTALLUILEVEL_BASIC | INSTALLUILEVEL_HIDECANCEL), 0); 
UINT uiStat = MsiInstallProduct(_T("example.msi"), NULL);

return 0;  
}
```



Um die Schaltfläche **Abbrechen** im Skript auszublenden, fügen Sie msiUILevelHideCancel zur [**UILevel-Eigenschaft**](installer-uilevel.md) des [**Installerobjekts hinzu.**](installer-object.md) Im folgenden VBScript-Beispiel wird die Schaltfläche **Abbrechen** ausgeblendet und Example.msi installiert.


```VB
Dim Installer As Object
Set Installer = CreateObject("WindowsInstaller.Installer")
Installer.UILevel = msiUILevelBasic + msiUILevelHideCancel
Installer.InstallProduct "example.msi"
```



## <a name="hiding-the-cancel-button-for-parts-of-an-installation-using-a-custom-action"></a>Ausblenden der Schaltfläche "Abbrechen" für Teile einer Installation mithilfe einer benutzerdefinierten Aktion

Ihre Installation kann die Schaltfläche **Abbrechen** während teilen einer Installation ausblenden und aufheben, indem sie eine INSTALLMESSAGE \_ COMMONDATA-Nachricht mithilfe einer benutzerdefinierten DLL-Aktion oder skripts sendet. Weitere Informationen finden Sie unter [Dynamic Link Libraries](dynamic-link-libraries.md), [Scripts](scripts.md), [Custom Actions](custom-actions.md)und Sending Messages to Windows Installer [Using MsiProcessMessage](sending-messages-to-windows-installer-using-msiprocessmessage.md).

Ein Aufruf einer benutzerdefinierten Aktion muss einen Datensatz bereitstellen. Feld 1 dieses Datensatzes muss den Wert 2 (zwei) enthalten, um die Schaltfläche **Abbrechen** anzugeben. Feld 2 muss entweder den Wert 0 oder 1 enthalten. Der Wert 0 in Feld 2 blendet die Schaltfläche aus, und der Wert 1 in Feld 2 entpackt die Schaltfläche. Beachten Sie, dass das Zuordnen eines Datensatzes der Größe 2 mit [**MsiCreateRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msicreaterecord) die Felder 0, 1 und 2 bereitstellt.

Die folgende benutzerdefinierte DLL-Beispielaktion blendet die Schaltfläche **Abbrechen** aus.


```C++
#include <windows.h>
#include <stdio.h>
#include <Shellapi.h>
#include <msi.h>
#include <Msiquery.h>

UINT __stdcall HideCancelButton(MSIHANDLE hInstall)
{
    PMSIHANDLE hRecord = MsiCreateRecord(2);
    if ( !hRecord)
        return ERROR_INSTALL_FAILURE;

    if (ERROR_SUCCESS != MsiRecordSetInteger(hRecord, 1, 2)
     || ERROR_SUCCESS != MsiRecordSetInteger(hRecord, 2, 0))
        return ERROR_INSTALL_FAILURE;

    MsiProcessMessage(hInstall, INSTALLMESSAGE_COMMONDATA, hRecord);

    return ERROR_SUCCESS;
}
```



Die folgende benutzerdefinierte VBScript-Aktion blendet die Schaltfläche **Abbrechen** aus.


```VB
Function HideCancelButton()

    Dim Record
    Set Record = Installer.CreateRecord(2)

    Record.IntegerData(1) = 2
    Record.IntegerData(2) = 0

    Session.Message msiMessageTypeCommonData, Record
 
    ' return success
    HideCancelButton = 1
    Exit Function

End Function
```



 

 



