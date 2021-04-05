---
description: In Windows 7 implementierte WMI die Win32 \_ optionalfeature-Klasse. Diese Klasse ruft den Status der optionalen Features auf, die auf einem Computer vorhanden sind.
ms.assetid: d756b0c0-b9f4-4b71-9f07-963a0dd5e585
ms.tgt_platform: multiple
title: Abfragen des Status optionaler Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c190b2a2143dae1e22c30b3e5e803908bcb4116
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755336"
---
# <a name="querying-the-status-of-optional-features"></a>Abfragen des Status optionaler Funktionen

In Windows 7 implementierte WMI die [**Win32 \_ optionalfeature**](/windows/desktop/CIMWin32Prov/win32-optionalfeature) -Klasse. Diese Klasse ruft den Status der optionalen Features auf, die auf einem Computer vorhanden sind.

Sie können Windows PowerShell-Cmdlets verwenden, um den Status optionaler Funktionen abzufragen. In allen Beispielen in diesem Thema wird das Cmdlet "Get-WmiObject" verwendet. Weitere Informationen finden Sie unter [Get-WMIObject](/previous-versions//dd315295(v=technet.10)).

**So rufen Sie alle Instanzen optionaler Features ab, die auf einem Computer vorhanden sind**

-   <span codelanguage="PowerShell"></span>
    <table>
    <colgroup>
    <col style="width: 100%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>PowerShell</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><pre><code>Get-WmiObject Win32_OptionalFeature</code></pre></td>
    </tr>
    </tbody>
    </table>

    

**So Fragen Sie eine optionale Funktion durch Angabe des Funktionsnamens ab**

-   <span codelanguage="PowerShell"></span>
    <table>
    <colgroup>
    <col style="width: 100%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>PowerShell</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><pre><code>Get-WmiObject -query &quot;select * from Win32_OptionalFeature where name = &#39;TelnetClient&#39;&quot;</code></pre></td>
    </tr>
    </tbody>
    </table>

    

    > [!Note]  
    > Bei der Eigenschaft **Name** wird die Groß-/Kleinschreibung beachtet

     

**So Fragen Sie optionale Features ab, indem Sie den Installationsstatus angeben**

-   <span codelanguage="PowerShell"></span>
    <table>
    <colgroup>
    <col style="width: 100%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>PowerShell</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><pre><code>Get-WmiObject -query &quot;select * from win32_optionalfeature where installstate= 1&quot;</code></pre></td>
    </tr>
    </tbody>
    </table>

    

    Weitere Informationen zu den möglichen Werten für die **InstallState** -Eigenschaft finden Sie unter [**Win32 \_ optionalfeature**](/windows/desktop/CIMWin32Prov/win32-optionalfeature).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Win32- \_ optionalfeature**](/windows/desktop/CIMWin32Prov/win32-optionalfeature)
</dt> </dl>

 

 
