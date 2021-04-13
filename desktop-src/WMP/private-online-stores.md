---
title: Private Online Stores
description: Private Online Stores
ms.assetid: c1e241f5-6d29-4b53-8be0-264597e03de7
keywords:
- Windows Media Player Online Stores, privat
- Online Stores, privat
- Typ 1 Online Stores, privat
- Typ 2 Online Stores, privat
- Private Online Stores
- Registrierung, private Online Stores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e11490a8a12659dfc1e2c5445167e8d71abaf00
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388496"
---
# <a name="private-online-stores"></a>Private Online Stores

Windows Media Player 10 oder höher unterstützt private Online Stores. Das heißt, Stores, die nur für bestimmte Benutzer sichtbar sind. Damit ein privater Onlinespeicher für den aktuellen Benutzer sichtbar ist, muss ein Eintrag vorhanden sein, der den privaten Online Store unter dem folgenden Registrierungsschlüssel darstellt.

HKEY \_ Current \_ User \\ Software \\ Microsoft \\ Media Player \\ privateservices

Der erforderliche Registrierungs Eintrag muss das folgende Format aufweisen:



| Name                                                         | type           | Wert                                                                     |
|--------------------------------------------------------------|----------------|---------------------------------------------------------------------------|
| Alle Namen, die von der Person ausgewählt werden, die den Registrierungs Eintrag erstellt | **REG \_ DWORD** | Eine von Microsoft bereitgestellte Zahl, die den privaten Onlinespeicher identifiziert. |



 

Das Windows Media Player 10-ActiveX-Steuerelement unterstützt private Online Stores nur, wenn das Steuerelement im Remote Modus ausgeführt wird. Das ActiveX-Steuerelement von Windows Media Player 11 unterstützt private Onlinespeicher, unabhängig davon, ob das Steuerelement im Remote Modus ausgeführt wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Informationen, die von Typ 1 und Typ 2 Online Stores gemeinsam sind**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> </dl>

 

 




