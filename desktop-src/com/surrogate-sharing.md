---
title: Freigabe von Ersatz Zeichen
description: DLL-Server geben ein Ersatz Zeichen frei, wenn Sie über übereinstimmende Sicherheits Identitäten verfügen und denselben AppID-Wert aufweisen.
ms.assetid: 88544be1-4716-47b6-9c08-2b5b2b178e1f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f6a934f03d42113cf73df4f059ac108801d21ea
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709425"
---
# <a name="surrogate-sharing"></a>Freigabe von Ersatz Zeichen

DLL-Server geben ein Ersatz Zeichen frei, wenn Sie über übereinstimmende Sicherheits Identitäten verfügen und denselben AppID-Wert aufweisen.

DLL-Server werden standardmäßig in ihren eigenen Ersatzprozess geladen. Wenn Sie andere DLL-Server in ein vorhandenes Ersatz Zeichen laden möchten, sodass mehr als ein dll-Server unterstützt wird, gibt es zwei Anforderungen:

-   Die DLL-Server müssen denselben AppID-Wert aufweisen.
-   Der Sicherheitskontext der DLL-Server muss identisch sein.

Wenn zwei dll-Server unter verschiedenen Sicherheits Identitäten gestartet werden sollen, müssen Sie sich in unterschiedlichen Surrogates befinden, unabhängig davon, ob Ihre APPIDs einander entsprechen.

Im folgenden finden Sie ein Beispiel für die Verwaltung der Freigabe von Ersatz Zeichen mit APPIDs:

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

Die beiden CLSIDs für die DLL-Komponenten comp1.dll und comp2.dll für die gemeinsame Verwendung einer AppID konfiguriert wurden. Der [AppID](appid-key.md) -Schlüssel gibt an, dass der DLL-Server in ein Ersatz Zeichen geladen werden kann, indem der [dllersatz](dllsurrogate.md) -Wert angegeben wird. In diesem Beispiel ist der **dllersatz** -Wert eine leere Zeichenfolge, die angibt, dass die standardmäßige System Implementierung des dll-Ersatz Zeichens verwendet werden soll.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DLL-Server Anforderungen](dll-server-requirements.md)
</dt> <dt>

[Registrieren des dll-Servers für die ersatzaktivierung](registering-the-dll-server-for-surrogate-activation.md)
</dt> </dl>

 

 




