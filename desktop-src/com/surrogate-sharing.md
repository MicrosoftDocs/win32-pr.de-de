---
title: Ersatzzeichenfreigabe
description: DLL-Server verwenden ein Ersatzzeichen, wenn sie über übereinstimmende Sicherheitsidentitäten und den gleichen AppID-Wert verfügen.
ms.assetid: 88544be1-4716-47b6-9c08-2b5b2b178e1f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34e159fff59144773633cfbe35bb1486e9eeb1014d02e23e0c9b95bcd817bb53
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119678410"
---
# <a name="surrogate-sharing"></a>Ersatzzeichenfreigabe

DLL-Server verwenden ein Ersatzzeichen, wenn sie über übereinstimmende Sicherheitsidentitäten und den gleichen AppID-Wert verfügen.

DLL-Server werden standardmäßig in ihren eigenen Ersatzprozess geladen. Es gibt zwei Anforderungen, um andere DLL-Server in ein vorhandenes Ersatzzeichen zu laden, sodass es mehrere DLL-Server unterstützt:

-   Die DLL-Server müssen den gleichen AppID-Wert aufweisen.
-   Der Sicherheitskontext der DLL-Server muss identisch sein.

Wenn zwei DLL-Server unter verschiedenen Sicherheitsidentitäten gestartet werden sollen, müssen sie sich in unterschiedlichen Ersatzzeichen befinden, unabhängig davon, ob ihre AppIDs übereinstimmen.

Es folgt ein Beispiel für die Verwaltung der Ersatzzeichenfreigabe mit AppIDs:

``` syntax
    AppID
        {12345678-0000-0000-0000-abcdabcdabcd}
            @DllSurrogate    REG_SZ
    CLSID
        {12345678-0000-0000-0000-000000000001}
            @AppId    REG_SZ    {12345678-0000-0000-0000-abcdabcdabcd}
            InProcServer32
    @    REG_SZ    c:\myapp\comp1.dll
        {12345678-0000-0000-0000-000000000002}
            @AppId    REG_SZ    {12345678-0000-0000-0000-abcdabcdabcd}
            InProcServer32
    @    REG_SZ    c:\myapp\comp2.dll
 
```

Die beiden CLSIDs für DLL-Komponenten comp1.dll und comp2.dll so konfiguriert, dass sie eine AppID gemeinsam nutzen. Der [AppID-Schlüssel](appid-key.md) gibt an, dass der DLL-Server durch Angabe des [DllSurrogate-Werts](dllsurrogate.md) in ein Ersatzzeichen geladen werden kann. In diesem Beispiel ist der **DllSurrogate-Wert** eine leere Zeichenfolge, die angibt, dass die Standardsystemimplementierung des DLL-Ersatzzeichens verwendet werden soll.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DLL-Serveranforderungen](dll-server-requirements.md)
</dt> <dt>

[Registrieren des DLL-Servers für die Ersatzaktivierung](registering-the-dll-server-for-surrogate-activation.md)
</dt> </dl>

 

 




