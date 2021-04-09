---
title: Senden eines Befehls
description: Senden eines Befehls
ms.assetid: 28c38f36-b6a7-44da-95e2-25b3dccefc84
keywords:
- mciSendString-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e69536b167b8fde648c3f3743058542d74bd8647
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103858195"
---
# <a name="sending-a-command"></a><span data-ttu-id="cb57b-104">Senden eines Befehls</span><span class="sxs-lookup"><span data-stu-id="cb57b-104">Sending a Command</span></span>

<span data-ttu-id="cb57b-105">Die folgende Beispiel Funktion sendet den [**Play**](play.md) -Befehl mit den Flags "from" und "to" mithilfe der Funktion " [**mciSendString**](/previous-versions//dd757161(v=vs.85)) ".</span><span class="sxs-lookup"><span data-stu-id="cb57b-105">The following example function sends the [**play**](play.md) command with the "from" and "to" flags using the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function.</span></span>


```C++
BOOL PlayFromTo(LPTSTR lpstrAlias, DWORD dwFrom, DWORD dwTo) 
{ 
    TCHAR achCommandBuff[128]; 
    int result;
    MCIERROR err;

    // Form the command string.
    result = _stprintf_s(
        achCommandBuff, 
        TEXT("play %s from %u to %u"), 
        lpstrAlias, dwFrom, dwTo); 

    if (result == -1)
    {
        return FALSE;
    }

    // Send the command string.
    err = mciSendString(achCommandBuff, NULL, 0, NULL); 
    if (err != 0)
    {
        return FALSE;
    }

    return TRUE;
} 
```



 

 