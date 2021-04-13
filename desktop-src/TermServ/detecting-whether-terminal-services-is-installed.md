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
# <a name="detecting-whether-the-remote-desktop-services-role-is-installed"></a>Erkennen, ob die Remotedesktopdienste Rolle installiert ist

Sie können die WMI-Klasse [**Win32 \_ Server Feature**](/windows/desktop/WmiSdk/win32-serverfeature) verwenden, um zu ermitteln, ob die Remotedesktopdienste Server-Rolle installiert ist.

Im folgenden c#-Beispiel wird eine Methode veranschaulicht, die **true** zurückgibt, wenn die Remotedesktopdienste Server-Rolle installiert ist und ausgeführt wird oder andernfalls **false** . Da die WMI-Klasse der Win32-Server [**\_ Funktion**](/windows/desktop/WmiSdk/win32-serverfeature) nur ab Windows Server 2008 verfügbar ist, ist dieser Code mit früheren Versionen von Windows nicht kompatibel.


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



 

 