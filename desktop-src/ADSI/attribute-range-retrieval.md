---
title: Attributbereichsabruf
description: Ein mehrwertiges Attribut kann über fast eine beliebige Anzahl von Werten verfügen. In vielen Fällen kann es vorteilhaft oder sogar notwendig sein, den Von einer Abfrage abgerufenen Wertebereich einzuschränken.
ms.assetid: 3a0eb764-fca9-4ca6-9991-b85f293961af
ms.tgt_platform: multiple
keywords:
- Attributbereichsabruf ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 994b1c4535ebce264386b088a53b730e679147f07b4bef9fe99d3a45a63461fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117840577"
---
# <a name="attribute-range-retrieval"></a>Attributbereichsabruf

Ein mehrwertiges Attribut kann über fast eine beliebige Anzahl von Werten verfügen. In vielen Fällen kann es vorteilhaft oder sogar notwendig sein, den Von einer Abfrage abgerufenen Wertebereich einzuschränken.

Der Bereichsabruf umfasst das Anfordern einer begrenzten Anzahl von Attributwerten in einer einzelnen Abfrage. Die Anzahl der angeforderten Werte muss kleiner oder gleich der maximalen Anzahl von Werten sein, die vom Server unterstützt werden. Um zu reduzieren, wie oft die Abfrage den Server kontaktieren muss, sollte die Anzahl der angeforderten Werte so nahe wie möglich an diesem Maximum liegen. Damit eine Anwendung ordnungsgemäß mit allen Windows-Servern funktioniert, sollte eine maximale Anzahl von 1.000 verwendet werden.

Die Bereichsspezifizierer für eine Eigenschaftenabfrage erfordern die folgende Form:


```C++
range=<low range>-<high range>
```



wobei &lt; "low &gt; range" der nullbasierte Index des ersten abzurufenden Eigenschaftswerts und &lt; "hoher &gt; Bereich" der nullbasierte Index des letzten abzurufenden Eigenschaftswerts ist. 0 (null) wird für &lt; "niedriger &gt; Bereich" verwendet, um den ersten Eintrag anzugeben. Das Platzhalterzeichen ( \* ) kann für "hoher Bereich" verwendet &lt; &gt; werden, um alle verbleibenden Einträge anzugeben.

In der folgenden Tabelle sind Beispiele für Bereichsspezifizierer aufgeführt.



| Beispiel      | Beschreibung                                                                                   |
|--------------|-----------------------------------------------------------------------------------------------|
| range=0-\*   | Rufen Sie alle Eigenschaftswerte ab. Dies unterliegt den vom Server vorgegebenen Grenzwerten.                |
| range=0-500  | Abrufen von Werten vom 1. bis zum 501. Inklusive.                                                |
| range=2-3    | Ruft den dritten und den 4. Wert ab.                                                                  |
| range=501-\* | Rufen Sie den 502. und alle verbleibenden Werte ab. Dies unterliegt den vom Server vorgegebenen Grenzwerten. |



 

Es gibt verschiedene Möglichkeiten, einen Bereich von Eigenschaftswerten abzurufen. Die [**IADs.GetInfoEx-Methode**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) kann entweder in einer Automatisierungssprache oder in C++ verwendet werden. Die **IADs.GetInfoEx-Methode** ist die bevorzugte Methode für den Bereichsabruf. Weitere Informationen zur Verwendung von **IADs.GetInfoEx** für den Bereichsabruf finden Sie unter [Verwenden von IADs::GetInfoEx für den Bereichsabruf.](using-iads--getinfoex-for-range-retrieval.md)

Wenn eine Automatisierungssprache verwendet wird, kann der ActiveX Directory Objects (ADO) verwendet werden, um einen Bereich von Eigenschaftswerten abzurufen. Weitere Informationen zur Verwendung von ADO für den Bereichsabruf finden Sie unter [Verwenden von ADO für den Bereichsabruf.](using-ado-for-range-retrieval.md)

Wenn C++ verwendet wird, können die Schnittstellen [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) und [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) verwendet werden, um einen Bereich von Eigenschaftswerten abzurufen. Weitere Informationen zur Verwendung von **IDirectorySearch** und **IDirectoryObject** für den Bereichsabruf finden Sie unter [Verwenden von IDirectorySearch und IDirectoryObject für den Bereichsabruf.](using-idirectorysearch-and-idirectoryobject-for-range-retrieval.md)

 

 




