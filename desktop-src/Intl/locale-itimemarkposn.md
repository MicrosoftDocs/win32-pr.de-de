---
description: Gebiets Schema \_ itimemarkposn
ms.assetid: 4aef2631-c05b-41e8-8f4d-f40da4143ab4
title: LOCALE_ITIMEMARKPOSN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0182235754d8f5b6b95bad6c58b4fee87d394d4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363859"
---
# <a name="locale_itimemarkposn"></a>Gebiets Schema \_ itimemarkposn

Spezifizierer, der angibt, ob die Zeit Marker-Zeichenfolge (am oder PM) der Zeit Zeichenfolge vorangestellt oder folgt. Der Registrierungs Wert ist "itimeprefix" für die Kompatibilität mit früheren asiatischen Versionen von Windows. Der Spezifizierer muss einen der folgenden Werte aufweisen. Es sind keine vom Benutzer angegebenen Werte zulässig. Es wird empfohlen, dass Ihre Anwendung die [locale \_ stimeformat](locale-stime-constants.md) -Konstante anstelle von locale \_ itimemarkposn verwendet.



| Wert | Bedeutung        |
|-------|----------------|
| 0     | Als Suffix verwenden. |
| 1     | Als Präfix verwenden. |



 

 

 



