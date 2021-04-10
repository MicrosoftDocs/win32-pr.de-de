---
title: Der Header der IDL-Schnittstelle
description: Der IDL-Schnittstellen Header gibt Informationen zur Schnittstelle als Ganzes an. Anders als bei der ACF enthält der Schnittstellen Header Attribute, die plattformunabhängig sind.
ms.assetid: 667e5228-3ea7-4910-90b9-999e6fd705e9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8abce6204fdc09ed74a63a85e9366125dbef8e35
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102282"
---
# <a name="the-idl-interface-header"></a>Der Header der IDL-Schnittstelle

Der IDL-Schnittstellen Header gibt Informationen zur Schnittstelle als Ganzes an. Anders als bei der ACF enthält der Schnittstellen Header Attribute, die plattformunabhängig sind.

Attribute im Schnittstellen Header sind global für die gesamte Schnittstelle. Das heißt, Sie gelten für die-Schnittstelle und alle zugehörigen Teile. Diese Attribute werden am Anfang der Schnittstellen Definition in eckige Klammern eingeschlossen. Ein Beispiel wird in der folgenden Schnittstellen Definition angezeigt:

``` syntax
[
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(1.0)
]
interface INTERFACENAME
{

}
```

Beachten Sie, dass der Schnittstellen Header das **\[** [**UUID**](/windows/desktop/Midl/uuid) **\]** -Attribut und das **\[** [**Version**](/windows/desktop/Midl/version) - **\]** Attribut enthält. Da diese die UUID und die Versionsnummer der-Schnittstelle darstellen, sind Sie Attribute der gesamten-Schnittstelle.

Der Schnittstellen Text kann auch Attribute enthalten. Sie sind jedoch nicht auf die gesamte Schnittstelle anwendbar. Sie verweisen auf bestimmte Elemente in der Schnittstelle, wie z. b. remote Prozedur Parameter.

Eine vollständige Erläuterung der IDL-Header Attribute finden Sie in der [Referenz zur Mittel l-Sprache](/windows/desktop/Midl/midl-language-reference).

 

 