---
title: /version_stamp Schalter
description: Der Schalter "/Version Stamp" unter \_ drückt die Generierung von Makros, die die mindestens erforderliche Versionsnummer der RPC-Header Datei "Rpcndr. h" angeben.
ms.assetid: ec03f68b-60f7-431e-9fba-4434ef082058
keywords:
- /version_stamp-Schalter-Mittel l
topic_type:
- apiref
api_name:
- /version_stamp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 704393dce869df4e5f715a1157cdb57967135e42
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "106338029"
---
# <a name="version_stamp-switch"></a>/Version \_ Stamp-Schalter

Der Schalter " **/Version \_ Stamp** " unterdrückt die Generierung von Makros, die die mindestens erforderliche Versionsnummer der RPC-Header Datei "Rpcndr. h" angeben.

Neue Mittelwert Funktionen erfordern möglicherweise zusätzliche Definitionen, um den Stub ordnungsgemäß zu kompilieren. der Stub verfügt daher über Makros, die die Kompatibilität zwischen den mittleren Binärdateien und der Buildumgebung überprüfen. Möglicherweise müssen Sie diesen Schalter verwenden, wenn Sie die mittlere Größe in eine andere Buildumgebung verschieben, als die, in der Sie zunächst die mittleren Binärdateien installiert haben.

Beachten Sie, dass das Mischen von Buildumgebungen nicht unterstützt wird

``` syntax
midl /version_stamp
```

## <a name="switch-options"></a>Optionen wechseln

Dieser Switch hat keine Parameter.

 

 




