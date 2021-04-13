---
title: /app_config Schalter
description: Der \_ Schalter/app config wählt den Anwendungs Konfigurations Modus aus, der es Ihnen ermöglicht, einige ACF-Schlüsselwörter in der IDL-Datei zu verwenden. Mit diesem Mittell-Compilerschalter können Sie die ACF weglassen und eine Schnittstelle in einer einzelnen IDL-Datei angeben.
ms.assetid: 8d12a0ed-7eaa-4ebc-a961-b726aefefadc
keywords:
- /app_config-Schalter-Mittel l
topic_type:
- apiref
api_name:
- /app_config
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 717d5234bd419fec7107a6d983ece026b4558935
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104389262"
---
# <a name="app_config-switch"></a>/APP \_ config-Schalter

Der Schalter **/App \_ config** wählt den Anwendungs Konfigurations Modus aus, der es Ihnen ermöglicht, einige ACF-Schlüsselwörter in der IDL-Datei zu verwenden. Mit diesem Mittell-Compilerschalter können Sie die ACF weglassen und eine Schnittstelle in einer einzelnen IDL-Datei angeben.

``` syntax
midl /app_config
```

## <a name="switch-options"></a>Optionen wechseln

Dieser Switch hat keine Parameter.

## <a name="remarks"></a>Bemerkungen

Microsoft RPC unterstützt die Verwendung der folgenden ACF-Attribute in der IDL-Datei:

-   Implizites \_ handle
-   Automatisches \_ handle
-   Explizites \_ handle

Zukünftige Versionen von Microsoft RPC unterstützen möglicherweise die Verwendung anderer ACF-Attribute in der IDL-Datei. Die Option **/App \_ config** stellt eine Microsoft-Erweiterung der OSF-DCE-Spezifikation dar und schließt sich daher mit der [**/OSF**](-osf.md) -Option gegenseitig aus.

Weitere Informationen, die sich auf den Schalter **/App \_ config** beziehen, finden Sie unter [Anwendungs Konfigurationsdatei (ACF)](application-configuration-file-acf-.md) und [Schnittstellen Definitionsdatei (IDL)](interface-definition-idl-file.md).

## <a name="examples"></a>Beispiele

**Mittel l/APP \_ config Dateiname. idl**

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Allgemeine Syntax der Mittell-Befehlszeile](general-midl-command-line-syntax.md)
</dt> </dl>

 

 




