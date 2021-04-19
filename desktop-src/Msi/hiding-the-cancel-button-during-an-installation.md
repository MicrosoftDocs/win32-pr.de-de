---
description: Sie können die Schaltfläche Abbrechen ausblenden, die verwendet wird, um eine Installation mit einer Befehlszeilenoption, der Windows Installer-API oder einer benutzerdefinierten Aktion abzubrechen. Je nachdem, welche Methode Sie verwenden, kann die Schaltfläche Abbrechen für einen Teil oder die gesamte Installation ausgeblendet werden.
ms.assetid: de2bb788-0d19-4818-8038-cae6000b38c4
title: Ausblenden der Schaltfläche "Abbrechen" während einer Installation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e55658bc69fe81b83b13d6c6ee7da84db77ad466
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106348703"
---
# <a name="hiding-the-cancel-button-during-an-installation"></a>Ausblenden der Schaltfläche "Abbrechen" während einer Installation

Sie können die Schaltfläche **Abbrechen** ausblenden, die verwendet wird, um eine Installation mit einer Befehlszeilenoption, der Windows Installer-API oder einer benutzerdefinierten Aktion abzubrechen. Je nachdem, welche Methode Sie verwenden, kann die Schaltfläche **Abbrechen** für einen Teil oder die gesamte Installation ausgeblendet werden.

## <a name="hiding-the-cancel-button-from-the-command-line"></a>Ausblenden der Schaltfläche "Abbrechen" in der Befehlszeile

Die Schaltfläche **Abbrechen** kann während der Installation mithilfe der Befehlszeilenoption (!) ausgeblendet werden. Dies kann nur für eine grundlegende Installation der Benutzeroberfläche (/QB) erfolgen. Die Schaltfläche **Abbrechen** ist für die gesamte Installation ausgeblendet. Weitere Informationen finden Sie unter [Befehlszeilenoptionen](command-line-options.md) und [Benutzeroberflächen Ebenen](user-interface-levels.md). Mit der folgenden Befehlszeile wird die Schaltfläche **Abbrechen** ausgeblendet und Example.msi installiert.

**msiexec/I example.msi/QB!**

## <a name="hiding-the-cancel-button-from-an-application-or-script"></a>Ausblenden der Schaltfläche "Abbrechen" in einer Anwendung oder einem Skript

Sie können eine Anwendung oder ein Skript schreiben, um die Schaltfläche " **Abbrechen** " auszublenden. Dies kann nur für eine einfache Installation auf Benutzeroberflächen Ebene erfolgen, sodass die Schaltfläche **Abbrechen** für die gesamte Installation ausgeblendet ist.

Wenn Sie die Schaltfläche Abbrechen in einer Anwendung ausblenden möchten, legen Sie für den Aufruf von " \_ [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui)" den Wert für "installuilevel Im folgenden Beispiel wird die Schaltfläche **Abbrechen** ausgeblendet und Example.msi installiert.


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



Um die Schaltfläche **Abbrechen** im Skript auszublenden, fügen Sie msiuilevelhidecancel der [**uilevel**](installer-uilevel.md) -Eigenschaft des [**Installer-Objekts**](installer-object.md)hinzu. Das folgende VBScript-Beispiel blendet die Schaltfläche **Abbrechen** aus und installiert Example.msi.


```VB
Dim Installer As Object
Set Installer = CreateObject("WindowsInstaller.Installer")
Installer.UILevel = msiUILevelBasic + msiUILevelHideCancel
Installer.InstallProduct "example.msi"
```



## <a name="hiding-the-cancel-button-for-parts-of-an-installation-using-a-custom-action"></a>Ausblenden der Schaltfläche "Abbrechen" für Teile einer Installation mithilfe einer benutzerdefinierten Aktion

Die Installation kann die Schaltfläche **Abbrechen** während der Teile einer Installation ausblenden und einblenden, indem eine installmessage \_ commondata-Nachricht mithilfe einer benutzerdefinierten DLL-Aktion oder Skripts gesendet wird. Weitere Informationen finden Sie unter [Dynamic Link Libraries](dynamic-link-libraries.md), [Scripts](scripts.md), [Custom Actions](custom-actions.md)und [send messages to Windows Installer using msiprocessmessage](sending-messages-to-windows-installer-using-msiprocessmessage.md).

Ein benutzerdefinierte Aktion muss einen Datensatz bereitstellen. Feld 1 dieses Datensatzes muss den Wert 2 (zwei) enthalten, um die Schaltfläche **Abbrechen** anzugeben. Feld 2 muss entweder den Wert 0 oder 1 enthalten. Der Wert 0 in Feld 2 blendet die Schaltfläche aus, und der Wert 1 in Feld 2 blendet die Schaltfläche aus. Beachten Sie, dass die Zuordnung eines Datensatzes der Größe 2 mit [**msikreaterecord**](/windows/desktop/api/Msiquery/nf-msiquery-msicreaterecord) die Felder 0, 1 und 2 bereitstellt.

Die folgende benutzerdefinierte DLL-Beispiel Aktion blendet die Schaltfläche **Abbrechen** aus.


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



 

 



