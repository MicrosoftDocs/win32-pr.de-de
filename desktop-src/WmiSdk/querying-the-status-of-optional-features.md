---
description: In Windows 7 hat WMI die Win32 \_ OptionalFeature-Klasse implementiert. Diese Klasse ruft den Status der optionalen Features ab, die auf einem Computer vorhanden sind.
ms.assetid: d756b0c0-b9f4-4b71-9f07-963a0dd5e585
ms.tgt_platform: multiple
title: Abfragen des Status optionaler Features
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec27457336adcc5c358aad0a5e139c1c7c07f6bcb72335ec549f9ca98cc1e5a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996030"
---
# <a name="querying-the-status-of-optional-features"></a>Abfragen des Status optionaler Features

In Windows 7 hat WMI die [**Win32 \_ OptionalFeature-Klasse**](/windows/desktop/CIMWin32Prov/win32-optionalfeature) implementiert. Diese Klasse ruft den Status der optionalen Features ab, die auf einem Computer vorhanden sind.

Sie können Windows PowerShell Cmdlets verwenden, um den Status optionaler Features abfragt. In allen Beispielen in diesem Thema wird das Cmdlet Get-WmiObject verwendet. Weitere Informationen finden Sie unter [Get-WmiObject](/previous-versions//dd315295(v=technet.10)).

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

    

**So fragen Sie ein optionales Feature ab, indem Sie den Featurenamen angeben**

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
    > Bei **der Name-Eigenschaft** wird die Schreibung beachtet.

     

**So fragen Sie optionale Features ab, indem Sie den Installationsstatus angeben**

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

    

    Weitere Informationen zu den möglichen Werten für die **InstallState-Eigenschaft** finden Sie unter [**Win32 \_ OptionalFeature**](/windows/desktop/CIMWin32Prov/win32-optionalfeature).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Win32 \_ OptionalFeature**](/windows/desktop/CIMWin32Prov/win32-optionalfeature)
</dt> </dl>

 

 
