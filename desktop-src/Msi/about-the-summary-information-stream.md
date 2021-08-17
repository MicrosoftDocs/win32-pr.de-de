---
description: Der Zusammenfassungsinformationsstream enthält Informationen zum Paket, die über den Microsoft Windows Explorer angezeigt werden können.
ms.assetid: b909955f-ddd6-4cf1-8e86-fcf89be80b41
title: Informationen zum Zusammenfassungsinformationsstream
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5178edc9fe2a94ddd2812abb8161c88423cc17cd033d228b066d5ce74b9f1694
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146033"
---
# <a name="about-the-summary-information-stream"></a>Informationen zum Zusammenfassungsinformationsstream

Der Zusammenfassungsinformationsstream enthält Informationen zum Paket, die über den Microsoft Windows Explorer angezeigt werden können. Auf diese Informationen kann über die **IStream-Schnittstelle zugegriffen** werden. Der Autor muss die Werte für jede dieser Eigenschaften bereitstellen.

Der Zusammenfassungsinformationsstream verwendet COM, um eine strukturierte Speicherung von Datenbanken zu ermöglichen. COM unterstützt das Konzept des strukturierten Speichers, auf den über die **IStream-Schnittstelle zugegriffen werden** kann. Der strukturierte Speicher unterstützt wiederum das Konzept von Eigenschaftssätzen als flexible Methode zum Serialisieren fast aller Informationen. Die COM-Spezifikation definiert einen einzelnen Standardeigenschaftssatz, Zusammenfassungsinformationen, der zum Auffüllen von Eigenschaftenblättern verwendet wird, die im Windows werden können. Daher können im Zusammenfassungsinformationsstream gespeicherte Informationen von Benutzern angezeigt werden, wenn sie mit der rechten Maustaste auf eine Installer-Datenbank klicken oder transformieren und Eigenschaften [auswählen.](about-properties.md)

Eine Liste der Zusammenfassungseigenschaftssatz finden Sie [unter Summary Information Stream Property Set](summary-information-stream-property-set.md).

Eine kurze Beschreibung der Eigenschaften von Zusammenfassungsinformationen, die mit Datenbanken, Transformationen und Patches verwendet werden, finden Sie unter [Zusammenfassungseigenschaftenbeschreibungen](summary-property-descriptions.md).

 

 



