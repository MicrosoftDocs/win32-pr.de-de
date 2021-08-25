---
title: Erkennen, ob die Remotedesktopdienste-Rolle installiert ist
description: C\-Codebeispiel, das eine Methode zeigt, die TRUE zurückgibt, wenn die Remotedesktopdienste-Serverrolle installiert ist und ausgeführt wird, andernfalls false, beginnend mit Windows Server 2008.
ms.assetid: 53ef8d43-2141-4df7-b9e6-baf0677924ba
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cf7ac1932c32ea797783d04f4e279bab03339c9b7620c11e72d4b755f084736
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119871760"
---
# <a name="detecting-whether-the-remote-desktop-services-role-is-installed"></a>Erkennen, ob die Remotedesktopdienste-Rolle installiert ist

Sie können die [**WMI-Klasse Win32 \_ ServerFeature**](/windows/desktop/WmiSdk/win32-serverfeature) verwenden, um zu ermitteln, ob Remotedesktopdienste Serverrolle installiert ist.

Das folgende C#-Beispiel zeigt eine Methode, die **True** zurückgibt, wenn Remotedesktopdienste Serverrolle installiert ist und ausgeführt wird, andernfalls **FALSE.** Da die WMI-Klasse [**\_ Win32 ServerFeature**](/windows/desktop/WmiSdk/win32-serverfeature) nur ab Windows Server 2008 verfügbar ist, ist dieser Code nicht mit früheren Versionen von Windows.


```CSharp
static void Main(string[] args)
{
    // 14 is the identifier of the Remote Desktop Services role.
    HasServerFeatureById(14);
}

static bool HasServerFeatureById(UInt32 roleId)
{
    try
    {
        ManagementClass serviceClass = new ManagementClass("Win32_ServerFeature");
        foreach (ManagementObject feature in serviceClass.GetInstances())
        {
            if ((UInt32)feature["ID"] == roleId)
            {
                return true;
            }
        }

        return false;
    }
    catch (ManagementException)
    {
        // The most likely cause of this is that this is being called from an 
        // operating system that is not a server operating system.
    }

    return false;
}

```



 

 