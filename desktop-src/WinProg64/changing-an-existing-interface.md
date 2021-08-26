---
title: Ändern einer vorhandenen Schnittstelle
description: Implementieren Sie nach Möglichkeit eine neue Schnittstelle für Ihre Anwendung, anstatt Änderungen an einer vorhandenen Schnittstelle vorzunehmen.
ms.assetid: 29845cf5-445c-403d-b298-d4e07c3536b7
keywords:
- Ändern vorhandener Schnittstellen mit 64-Bit-Windows-Programmierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 782587471de5616750501552445599a94571ff2275d080347937c595e2cd7668
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119899070"
---
# <a name="changing-an-existing-interface"></a>Ändern einer vorhandenen Schnittstelle

Implementieren Sie nach Möglichkeit eine neue Schnittstelle für Ihre Anwendung, anstatt Änderungen an einer vorhandenen Schnittstelle vorzunehmen. Wenn Sie das Ändern einer vorhandenen Schnittstelle nicht vermeiden können, verwenden Sie neue Datentypen nur in neuen Methoden. Die Einführung eines neuen Datentyps oder das Ändern eines vorhandenen Typs ist die häufigste Ursache für Inkompatibilitätsprobleme. Das RPC-Laufzeitmodell geht davon aus, dass die empfangende Anwendung die Empfangenden Datentypen kennt, sodass Daten ohne generische Datenbeschreibung in die Leitung gestellt werden. Wenn der Empfänger einen anderen Datentyp als den erwartet, den der Absender an die Übertragung übermittelt hat, löst der Stub eine Ausnahme aus (oder die Übertragung schlägt auf andere, weniger ordnungsgemäße Weise fehl).

Eine RPC-Schnittstelle wird durch ihre UUID und ihre Haupt- und Nebenversionsnummern definiert. Wenn Sie eine vorhandene Schnittstelle ändern, sollten Sie die neuen Methoden am Ende der Schnittstelle hinzufügen und die Nebenversionsnummer ändern. Wenn Sie Methoden an einer anderen Stelle hinzufügen oder andere Änderungen an der Schnittstelle vornehmen, müssen Sie auch die Hauptversionsnummer ändern.

Realistisch gesehen gibt es Zeiten, in denen Sie nicht einmal die Nebenversionsnummer ändern können, da ein neuer Client nicht mit einem alten Server kommunizieren kann und Sie den Server nicht aktualisieren können. Die RPC-Laufzeit löst eine Ausnahme (RPC \_ S \_ PROCNUM \_ OUT OF \_ \_ RANGE) aus, wenn ein Client eine Methode aufruft, die über die für seine Schnittstelle mit dem Server angegebenen hinausgeht. Die Problemumgehung besteht darin, die Versionsnummern unverändert zu lassen und Ihren Clientcode zu schreiben, um diese Ausnahme ordnungsgemäß zu behandeln– z. B. durch den Client, der seine Leistung beeinträchtigt, oder durch die für Ihre Anwendung geeigneten Mittel.

Es gibt eine ähnliche Problemumgehung für einen speziellen Fall, bei dem ein Datentyp in einer vorhandenen Methode geändert wird. Wenn Sie über eine [**Union**](/windows/desktop/Midl/union) verfügen, deren Verzweigungen Zeiger sind und die keine Standardverzweigung für nicht erkannte Typen hat, können Sie eine neue Verzweigung hinzufügen, die den neuen Datentyp verwendet. Dadurch wird die Größe der Datenstruktur nicht geändert. Wenn Ihr Client mit einem neuen Server spricht, kann er den neuen Datentyp verwenden. Wenn Ihr Client jedoch mit einem alten Server spricht, wird die Ausnahme RPC S INVALID TAG durch die Laufzeit \_ \_ \_ ausgelöst. Auch hier müssen Sie Ihren Clientcode schreiben, um diese Ausnahme entsprechend zu behandeln.

Eine DCOM-Schnittstelle wird durch ihre GUID identifiziert. In DCOM gelten Schnittstellen als unveränderlich, und Sie können Änderungen nur vornehmen, indem Sie eine neue Schnittstelle erstellen, die von der alten erbt. Diese Regeln stellen sicher, dass Clients und Server kompatibel bleiben.

 

 