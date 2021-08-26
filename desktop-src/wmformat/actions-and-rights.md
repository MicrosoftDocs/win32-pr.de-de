---
title: Aktionen und Rechte
description: Aktionen und Rechte
ms.assetid: 711c6a04-6c40-4ea5-8c4f-91d000286b7b
keywords:
- Windows Media Format SDK, Digital Rights Management (DRM)
- Windows Medienformat-SDK, DRM-Lizenzen
- Windows Media Format SDK,Lizenzen für DRM
- Digital Rights Management (DRM), Aktionen
- DRM (Digital Rights Management), Aktionen
- Digital Rights Management (DRM), Rechte
- DRM (Digital Rights Management), Rechte
- Digital Rights Management (DRM), Lizenzen
- DRM (Digital Rights Management), Lizenzen
- licenses,DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b822c0350af12c5e266570a031ca0d3eda7c99b4b8451b751786a60a4a0908d6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089770"
---
# <a name="actions-and-rights"></a>Aktionen und Rechte

Wenn eine Datei mithilfe von Windows Media DRM geschützt wird, ist ihre Verwendung vollständig eingeschränkt. Lizenzen können ausgestellt werden, um einem Benutzer die Verwendung des Inhalts auf bestimmte Weise zu ermöglichen. Jede Art und Weise, wie ein Benutzer den Inhalt verwenden kann, wird durch eine Aktion beschrieben. Die Wiedergabe einer Datei auf einem Computer ist beispielsweise eine Aktion.

Eine Lizenz, die eine bestimmte Aktion ermöglicht, wird als Gewährung eines Rechts bezeichnet. Beispielsweise kann eine Lizenz das Recht gewähren, Inhalte auf einem Computer wiederzuspielen.

Aktionen und Rechte beziehen sich auf die gleichen Methoden zur Verwendung von Inhalten. Der Unterschied ist, dass die Aktion auf die Verwendung verweist, während das Recht auf die Berechtigung verweist. Trotz dieses Unterschieds werden die Wörter action und right häufig synonym in dieser Dokumentation und in anderen Dokumenten verwendet, die Windows Media DRM beschreiben.

Die Aktionen, die Windows Media DRM-Rechten unterliegen, sind im Abschnitt [Rechtekonst constants](rights-constants.md) dieser Dokumentation aufgeführt.

Bestimmte Methoden der erweiterten APIs Windows Media DRM Client verwenden unterschiedliche Konstanten, um auf die grundlegenden DRM-Rechte zu verweisen. Beispielsweise verwendet die [**IWMDRMLicenseQuery::QueryLicenseState-Methode**](iwmdrmlicensequery-querylicensestate.md) einen Satz von Zeichenfolgen, die für Lizenzzustände spezifisch sind. Obwohl diese Konstanten andere Zeichenfolgen als die grundlegenden Rechtekonst constants definieren, verweisen sie auf die gleichen Rechte in der Lizenz.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Konzepte**](drmconcepts.md)
</dt> </dl>

 

 




