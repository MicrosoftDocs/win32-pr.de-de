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
# <a name="hiding-the-cancel-button-during-an-installation"></a><span data-ttu-id="bdd16-104">Ausblenden der Schaltfläche "Abbrechen" während einer Installation</span><span class="sxs-lookup"><span data-stu-id="bdd16-104">Hiding the Cancel Button During an Installation</span></span>

<span data-ttu-id="bdd16-105">Sie können die Schaltfläche **Abbrechen** ausblenden, die verwendet wird, um eine Installation mit einer Befehlszeilenoption, der Windows Installer-API oder einer benutzerdefinierten Aktion abzubrechen.</span><span class="sxs-lookup"><span data-stu-id="bdd16-105">You can hide the **Cancel** button that is used to cancel an installation by using a command-line option, the Windows Installer API, or a custom action.</span></span> <span data-ttu-id="bdd16-106">Je nachdem, welche Methode Sie verwenden, kann die Schaltfläche **Abbrechen** für einen Teil oder die gesamte Installation ausgeblendet werden.</span><span class="sxs-lookup"><span data-stu-id="bdd16-106">The **Cancel** button can be hidden for part or all of the installation depending on which method you use.</span></span>

## <a name="hiding-the-cancel-button-from-the-command-line"></a><span data-ttu-id="bdd16-107">Ausblenden der Schaltfläche "Abbrechen" in der Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="bdd16-107">Hiding the Cancel Button from the Command Line</span></span>

<span data-ttu-id="bdd16-108">Die Schaltfläche **Abbrechen** kann während der Installation mithilfe der Befehlszeilenoption (!) ausgeblendet werden.</span><span class="sxs-lookup"><span data-stu-id="bdd16-108">The **Cancel** button can be hidden during installation by using the (!) command-line option.</span></span> <span data-ttu-id="bdd16-109">Dies kann nur für eine grundlegende Installation der Benutzeroberfläche (/QB) erfolgen.</span><span class="sxs-lookup"><span data-stu-id="bdd16-109">This can only be done for a basic user interface level installation (/qb).</span></span> <span data-ttu-id="bdd16-110">Die Schaltfläche **Abbrechen** ist für die gesamte Installation ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="bdd16-110">The **Cancel** button is hidden for the entire installation.</span></span> <span data-ttu-id="bdd16-111">Weitere Informationen finden Sie unter [Befehlszeilenoptionen](command-line-options.md) und [Benutzeroberflächen Ebenen](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="bdd16-111">For more information, see [Command-Line Options](command-line-options.md) and [User Interface Levels](user-interface-levels.md).</span></span> <span data-ttu-id="bdd16-112">Mit der folgenden Befehlszeile wird die Schaltfläche **Abbrechen** ausgeblendet und Example.msi installiert.</span><span class="sxs-lookup"><span data-stu-id="bdd16-112">The following command line hides the **Cancel** button and installs Example.msi.</span></span>

<span data-ttu-id="bdd16-113">**msiexec/I example.msi/QB!**</span><span class="sxs-lookup"><span data-stu-id="bdd16-113">**msiexec /I example.msi /qb!**</span></span>

## <a name="hiding-the-cancel-button-from-an-application-or-script"></a><span data-ttu-id="bdd16-114">Ausblenden der Schaltfläche "Abbrechen" in einer Anwendung oder einem Skript</span><span class="sxs-lookup"><span data-stu-id="bdd16-114">Hiding the Cancel Button from an Application or Script</span></span>

<span data-ttu-id="bdd16-115">Sie können eine Anwendung oder ein Skript schreiben, um die Schaltfläche " **Abbrechen** " auszublenden.</span><span class="sxs-lookup"><span data-stu-id="bdd16-115">You can write an application or script to hide the **Cancel** button.</span></span> <span data-ttu-id="bdd16-116">Dies kann nur für eine einfache Installation auf Benutzeroberflächen Ebene erfolgen, sodass die Schaltfläche **Abbrechen** für die gesamte Installation ausgeblendet ist.</span><span class="sxs-lookup"><span data-stu-id="bdd16-116">This can only be done for a basic UI level installation so that the **Cancel** button is hidden for the entire installation.</span></span>

<span data-ttu-id="bdd16-117">Wenn Sie die Schaltfläche Abbrechen in einer Anwendung ausblenden möchten, legen Sie für den Aufruf von " \_ [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui)" den Wert für "installuilevel</span><span class="sxs-lookup"><span data-stu-id="bdd16-117">To hide the Cancel button from an application, set INSTALLUILEVEL\_HIDECANCEL when calling [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui).</span></span> <span data-ttu-id="bdd16-118">Im folgenden Beispiel wird die Schaltfläche **Abbrechen** ausgeblendet und Example.msi installiert.</span><span class="sxs-lookup"><span data-stu-id="bdd16-118">The following example hides the **Cancel** button and installs Example.msi.</span></span>


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



<span data-ttu-id="bdd16-119">Um die Schaltfläche **Abbrechen** im Skript auszublenden, fügen Sie msiuilevelhidecancel der [**uilevel**](installer-uilevel.md) -Eigenschaft des [**Installer-Objekts**](installer-object.md)hinzu.</span><span class="sxs-lookup"><span data-stu-id="bdd16-119">To hide the **Cancel** button from script, add msiUILevelHideCancel to the [**UILevel**](installer-uilevel.md) property of the [**Installer Object**](installer-object.md).</span></span> <span data-ttu-id="bdd16-120">Das folgende VBScript-Beispiel blendet die Schaltfläche **Abbrechen** aus und installiert Example.msi.</span><span class="sxs-lookup"><span data-stu-id="bdd16-120">The following VBScript sample hides the **Cancel** button and installs Example.msi.</span></span>


```VB
Dim Installer As Object
Set Installer = CreateObject("WindowsInstaller.Installer")
Installer.UILevel = msiUILevelBasic + msiUILevelHideCancel
Installer.InstallProduct "example.msi"
```



## <a name="hiding-the-cancel-button-for-parts-of-an-installation-using-a-custom-action"></a><span data-ttu-id="bdd16-121">Ausblenden der Schaltfläche "Abbrechen" für Teile einer Installation mithilfe einer benutzerdefinierten Aktion</span><span class="sxs-lookup"><span data-stu-id="bdd16-121">Hiding the Cancel Button for Parts of an Installation Using a Custom Action</span></span>

<span data-ttu-id="bdd16-122">Die Installation kann die Schaltfläche **Abbrechen** während der Teile einer Installation ausblenden und einblenden, indem eine installmessage \_ commondata-Nachricht mithilfe einer benutzerdefinierten DLL-Aktion oder Skripts gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="bdd16-122">Your installation can hide and unhide the **Cancel** button during parts of an installation by sending an INSTALLMESSAGE\_COMMONDATA message using a DLL custom action or scripts.</span></span> <span data-ttu-id="bdd16-123">Weitere Informationen finden Sie unter [Dynamic Link Libraries](dynamic-link-libraries.md), [Scripts](scripts.md), [Custom Actions](custom-actions.md)und [send messages to Windows Installer using msiprocessmessage](sending-messages-to-windows-installer-using-msiprocessmessage.md).</span><span class="sxs-lookup"><span data-stu-id="bdd16-123">For more information, see [Dynamic-Link Libraries](dynamic-link-libraries.md), [Scripts](scripts.md), [Custom Actions](custom-actions.md), and [Sending Messages to Windows Installer Using MsiProcessMessage](sending-messages-to-windows-installer-using-msiprocessmessage.md).</span></span>

<span data-ttu-id="bdd16-124">Ein benutzerdefinierte Aktion muss einen Datensatz bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="bdd16-124">A call to a custom action must provide a record.</span></span> <span data-ttu-id="bdd16-125">Feld 1 dieses Datensatzes muss den Wert 2 (zwei) enthalten, um die Schaltfläche **Abbrechen** anzugeben.</span><span class="sxs-lookup"><span data-stu-id="bdd16-125">Field 1 of this record must contain the value 2 (two) to specify the **Cancel** button.</span></span> <span data-ttu-id="bdd16-126">Feld 2 muss entweder den Wert 0 oder 1 enthalten.</span><span class="sxs-lookup"><span data-stu-id="bdd16-126">Field 2 must contain either the value 0 or 1.</span></span> <span data-ttu-id="bdd16-127">Der Wert 0 in Feld 2 blendet die Schaltfläche aus, und der Wert 1 in Feld 2 blendet die Schaltfläche aus.</span><span class="sxs-lookup"><span data-stu-id="bdd16-127">A value of 0 in Field 2 hides the button and a value of 1 in Field 2 unhides the button.</span></span> <span data-ttu-id="bdd16-128">Beachten Sie, dass die Zuordnung eines Datensatzes der Größe 2 mit [**msikreaterecord**](/windows/desktop/api/Msiquery/nf-msiquery-msicreaterecord) die Felder 0, 1 und 2 bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="bdd16-128">Note that allocating a record of size 2 with [**MsiCreateRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msicreaterecord) provides fields 0, 1, and 2.</span></span>

<span data-ttu-id="bdd16-129">Die folgende benutzerdefinierte DLL-Beispiel Aktion blendet die Schaltfläche **Abbrechen** aus.</span><span class="sxs-lookup"><span data-stu-id="bdd16-129">The following sample DLL custom action hides the **Cancel** button.</span></span>


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



<span data-ttu-id="bdd16-130">Die folgende benutzerdefinierte VBScript-Aktion blendet die Schaltfläche **Abbrechen** aus.</span><span class="sxs-lookup"><span data-stu-id="bdd16-130">The following VBScript Custom Action hides the **Cancel** button.</span></span>


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



 

 



