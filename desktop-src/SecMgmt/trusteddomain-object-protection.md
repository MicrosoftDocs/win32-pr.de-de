---
description: Wenn ein TrustedDomain-Objekt erstellt wird, wird ihm ein Standardschutz zugewiesen.
ms.assetid: cc554630-7be7-4657-90f2-ce5fa81731b2
title: TrustedDomain Object Protection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3e34eac9b9e3a021db7580803cec6c99f6489d01c9499b28251cb262b721fd3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004798"
---
# <a name="trusteddomain-object-protection"></a>TrustedDomain Object Protection

Wenn ein [**TrustedDomain-Objekt**](trusteddomain-object.md) erstellt wird, wird ihm wie folgt ein Standardschutz zugewiesen:

-   Der lokalen GRUPPE WORLD wird GENERIC \_ EXECUTE-Zugriff gewährt.
-   Der lokalen Gruppe LOCAL \_ ADMIN wird DELETE-, GENERIC \_ READ-, GENERIC \_ WRITE- und GENERIC \_ EXECUTE-Zugriff gewährt.
-   Die lokale Gruppe LOCAL \_ ADMIN wird als Besitzer und primäre Gruppe des Objekts zugewiesen.

 

 



