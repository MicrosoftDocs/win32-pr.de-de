---
title: HTML-Ressource
description: Definiert eine HTML-Datei.
ms.assetid: d3cf8348-8c10-41d9-a061-cdce0e13abf4
keywords:
- HTML-Ressourcen Menüs und andere Ressourcen
topic_type:
- apiref
api_name:
- HTML
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9db6477aed5180ae18b99f53f4ebadf9d0ad0c91
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "103857495"
---
# <a name="html-resource"></a>HTML-Ressource

Definiert eine HTML-Datei.

``` syntax
nameID HTML filename
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*NameID*
</dt> <dd>

Eindeutiger Name oder ein 16-Bit-Ganzzahl-Wert ohne Vorzeichen, der die Ressource identifiziert.

</dd> <dt>

<span id="filename"></span><span id="FILENAME"></span>*Einfügen*
</dt> <dd>

Der Name der HTML-Datei. Wenn sich die Datei nicht im aktuellen Arbeitsverzeichnis befindet, muss Sie ein vollständiger oder relativer Pfad sein. Der Pfad muss eine Zeichenfolge in Anführungszeichen sein.

</dd> </dl>

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird eine HTML-Ressource definiert:

``` syntax
ID_RESPONSE_ERROR_PAGE  HTML "res\\responseerorpage.htm"
```

 

 




