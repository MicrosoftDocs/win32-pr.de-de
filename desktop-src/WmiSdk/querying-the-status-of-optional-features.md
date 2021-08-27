---
description: In Windows 7 hat WMI die Win32 \_ OptionalFeature-Klasse implementiert. Diese Klasse ruft den Status der optionalen Features ab, die auf einem Computer vorhanden sind.
ms.assetid: d756b0c0-b9f4-4b71-9f07-963a0dd5e585
ms.tgt_platform: multiple
title: Abfragen des Status optionaler Features
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ecffe6ddbe9b860c6f49fe12d3fed500c169bef
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476706"
---
# <a name="querying-the-status-of-optional-features"></a>Abfragen des Status optionaler Features

In Windows 7 hat WMI die [**Win32 \_ OptionalFeature-Klasse**](/windows/desktop/CIMWin32Prov/win32-optionalfeature) implementiert. Diese Klasse ruft den Status der optionalen Features ab, die auf einem Computer vorhanden sind.

Sie können Windows PowerShell Cmdlets verwenden, um den Status optionaler Features abzufragen. In allen Beispielen in diesem Thema wird das Cmdlet Get-WmiObject verwendet. Weitere Informationen finden Sie unter [Get-WmiObject.](/previous-versions//dd315295(v=technet.10))

**So rufen Sie alle Instanzen optionaler Features ab, die auf einem Computer vorhanden sind**

-   <span codelanguage="PowerShell"></span>
    
| PowerShell | 
|------------|
| <pre><code>Get-WmiObject Win32_OptionalFeature</code></pre> | 


    

**So fragen Sie ein optionales Feature ab, indem Sie den Featurenamen angeben**

-   <span codelanguage="PowerShell"></span>
    
| PowerShell | 
|------------|
| <pre><code>Get-WmiObject -query "select * from Win32_OptionalFeature where name = 'TelnetClient'"</code></pre> | 


    

    > [!Note]  
    > The **name** property is case-sensitive.

     

**So fragen Sie optionale Features ab, indem Sie den Installationsstatus angeben**

-   <span codelanguage="PowerShell"></span>
    
| PowerShell | 
|------------|
| <pre><code>Get-WmiObject -query "select * from win32_optionalfeature where installstate= 1"</code></pre> | 


    

    For more information about the possible values for the **InstallState** property, see [**Win32\_OptionalFeature**](/windows/desktop/CIMWin32Prov/win32-optionalfeature).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Win32 \_ OptionalFeature**](/windows/desktop/CIMWin32Prov/win32-optionalfeature)
</dt> </dl>

 

 
