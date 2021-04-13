---
title: Erkennen, ob die Remotedesktopdienste Rolle installiert ist
description: C \ Codebeispiel, das eine Methode anzeigt, die true zurückgibt, wenn die Remotedesktopdienste Server-Rolle installiert ist und ausgeführt wird oder andernfalls false ist, beginnend mit Windows Server 2008.
ms.assetid: 53ef8d43-2141-4df7-b9e6-baf0677924ba
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49f7d094f88271346c97f8d0467b48a266c865d5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390789"
---
# <a name="detecting-whether-the-remote-desktop-services-role-is-installed"></a><span data-ttu-id="7c809-103">Erkennen, ob die Remotedesktopdienste Rolle installiert ist</span><span class="sxs-lookup"><span data-stu-id="7c809-103">Detecting Whether the Remote Desktop Services Role Is Installed</span></span>

<span data-ttu-id="7c809-104">Sie können die WMI-Klasse [**Win32 \_ Server Feature**](/windows/desktop/WmiSdk/win32-serverfeature) verwenden, um zu ermitteln, ob die Remotedesktopdienste Server-Rolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="7c809-104">You can use the [**Win32\_ServerFeature**](/windows/desktop/WmiSdk/win32-serverfeature) WMI class to detect whether the Remote Desktop Services server role is installed.</span></span>

<span data-ttu-id="7c809-105">Im folgenden c#-Beispiel wird eine Methode veranschaulicht, die **true** zurückgibt, wenn die Remotedesktopdienste Server-Rolle installiert ist und ausgeführt wird oder andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="7c809-105">The following C# example shows a method that returns **True** if the Remote Desktop Services server role is installed and running or **false** otherwise.</span></span> <span data-ttu-id="7c809-106">Da die WMI-Klasse der Win32-Server [**\_ Funktion**](/windows/desktop/WmiSdk/win32-serverfeature) nur ab Windows Server 2008 verfügbar ist, ist dieser Code mit früheren Versionen von Windows nicht kompatibel.</span><span class="sxs-lookup"><span data-stu-id="7c809-106">Because the [**Win32\_ServerFeature**](/windows/desktop/WmiSdk/win32-serverfeature) WMI class is only available beginning with Windows Server 2008, this code is not compatible with earlier versions of Windows.</span></span>


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



 

 