---
description: Der Datenstrom für Zusammenfassungs Informationen enthält Informationen über das Paket, das über Microsoft Windows-Explorer angezeigt werden kann.
ms.assetid: b909955f-ddd6-4cf1-8e86-fcf89be80b41
title: Informationen zum Datenstrom für Zusammenfassungs Informationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ab931d7f9b6dd726fc6df3d7b805f4cc5c25caa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131509"
---
# <a name="about-the-summary-information-stream"></a>Informationen zum Datenstrom für Zusammenfassungs Informationen

Der Datenstrom für Zusammenfassungs Informationen enthält Informationen über das Paket, das über Microsoft Windows-Explorer angezeigt werden kann. Diese Informationen sind über die **IStream** -Schnittstelle zugänglich. Der Autor muss die Werte für jede dieser Eigenschaften angeben.

Der Zusammenfassungs Datenstrom verwendet com, um eine strukturierte Speicherung von Datenbanken bereitzustellen. COM unterstützt das Konzept des strukturierten Speichers, der über die **IStream** -Schnittstelle zugänglich ist. Die strukturierte Speicherung unterstützt wiederum das Konzept der Eigenschaften Sätze als flexible Methode für die Serialisierung von fast allen Informationen. Die com-Spezifikation definiert einen einzelnen Standardeigenschaften Satz, zusammenfassende Informationen, der verwendet wird, um die von Windows-Explorer sichtbaren Eigenschaften Blätter aufzufüllen. Daher können die im Zusammenfassungs Datenstrom gespeicherten Informationen von Benutzern angezeigt werden, wenn Sie mit der rechten Maustaste auf eine Installerdatenbank oder eine Transformation klicken und [Eigenschaften](about-properties.md)auswählen.

Eine Liste der Zusammenfassungs Eigenschaften Satzes finden Sie unter [Summary Information Stream-Eigenschaften Satz](summary-information-stream-property-set.md).

Eine kurze Beschreibung der Eigenschaften der Zusammenfassungs Informationen, die mit Datenbanken, Transformationen und Patches verwendet werden, finden Sie unter [Summary Property-Beschreibungen](summary-property-descriptions.md).

 

 



