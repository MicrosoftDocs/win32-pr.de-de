---
title: /Win64-Schalter
description: Der/Win64-Schalter weist den Mittelwert Compiler an, Stub-Dateien oder eine Typbibliotheks Datei für eine 64-Bit-Umgebung zu generieren. Beachten Sie, dass dieser Schalter veraltet ist.
ms.assetid: 6f4780d3-6415-42af-a8ee-3884a8cebe26
keywords:
- /Win64-Schalter-Mittel l
topic_type:
- apiref
api_name:
- /win64
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e61906126607c0a8d4b81ef76805bb4b7e0d4145
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104312299"
---
# <a name="win64-switch"></a>/Win64-Schalter

Der **/Win64** -Schalter weist den Mittelwert Compiler an, Stub-Dateien oder eine Typbibliotheks Datei für eine 64-Bit-Umgebung zu generieren.

> [!Note]  
> Dieser Schalter ist veraltet. Verwenden Sie stattdessen den Schalter " [**/ia64**](-ia64.md) " oder " [**/amd64**](-amd64.md) ". Der Schalter " **/Win64** " entspricht dem Schalter " **/ia64** ".

 

``` syntax
midl /win64
```

## <a name="switch-options"></a>Optionen wechseln

Dieser Switch hat keine Parameter.

## <a name="remarks"></a>Bemerkungen

Der Schalter **/Win64** entspricht dem Festlegen des [**/env**](-env.md) -Schalters auf Win64.

> [!Note]  
> Es ist nicht möglich, mit MIDL.exe einen 64-Bit-TLB unter Windows 2000 zu entwickeln.

 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**/ENV**](-env.md)
</dt> <dt>

[**/ia64**](-ia64.md)
</dt> <dt>

[**/amd64**](-amd64.md)
</dt> </dl>

 

 




