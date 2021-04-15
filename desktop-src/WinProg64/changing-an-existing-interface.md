---
title: Ändern einer vorhandenen Schnittstelle
description: Implementieren Sie nach Möglichkeit eine neue Schnittstelle für Ihre Anwendung, anstatt Änderungen an einer vorhandenen Anwendung vorzunehmen.
ms.assetid: 29845cf5-445c-403d-b298-d4e07c3536b7
keywords:
- Ändern vorhandener Schnittstellen 64-Bit-Windows-Programmierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51a656ee768dcc2e88725d2cff0ddc5604fd771f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104516919"
---
# <a name="changing-an-existing-interface"></a>Ändern einer vorhandenen Schnittstelle

Implementieren Sie nach Möglichkeit eine neue Schnittstelle für Ihre Anwendung, anstatt Änderungen an einer vorhandenen Anwendung vorzunehmen. Wenn Sie die Änderung einer vorhandenen Schnittstelle nicht vermeiden können, verwenden Sie neue Datentypen nur in neuen Methoden. Das Einführen eines neuen Datentyps oder das Ändern eines vorhandenen Typs ist die häufigste Quelle für Inkompatibilitäts Probleme. Das RPC-Lauf Zeitmodell geht davon aus, dass die empfangende Anwendung die Datentypen kennt, die Sie empfängt, sodass Daten ohne generische Daten Beschreibung in das Netzwerk eingefügt werden. Wenn der Empfänger einen anderen Datentyp erwartet als den Absender, den der Absender eingegeben hat, löst der Stub eine Ausnahme aus (oder die Übertragung schlägt in anderer Weise weniger ordnungsgemäß vor).

Eine RPC-Schnittstelle wird durch die UUID und die Haupt-und neben Versionsnummern definiert. Wenn Sie eine vorhandene Schnittstelle ändern, sollten Sie die neuen Methoden am Ende der Schnittstelle hinzufügen und die neben Versionsnummer ändern. Wenn Sie an einem anderen Ort Methoden hinzufügen oder andere Änderungen an der Schnittstelle vornehmen, müssen Sie auch die Hauptversionsnummer ändern.

Normalerweise gibt es Zeiten, in denen Sie sogar die neben Versionsnummer nicht ändern können, da ein neuer Client nicht mit einem alten Server kommunizieren kann und Sie den Server nicht aktualisieren können. Die RPC-Laufzeit löst eine Ausnahme aus, die RPC \_ S \_ procnum \_ außerhalb \_ des gültigen \_ Bereichs, wenn ein Client eine Methode aufruft, die über diejenigen hinausgeht, die für die Schnittstelle mit dem Server angegeben sind. Die Problem Umgehung besteht darin, die Versionsnummern unverändert zu lassen und den Client Code zu schreiben, um diese Ausnahme ordnungsgemäß zu behandeln – durch den Client, wodurch die Leistung herabgestuft wird, z. b. oder durch die für Ihre Anwendung geeigneten Mittel.

Es gibt eine ähnliche Problem Umgehung für einen besonderen Fall, dass ein Datentyp in einer vorhandenen Methode geändert wird. Wenn Sie über eine [**Union**](/windows/desktop/Midl/union) verfügen, deren Verzweigungen Zeiger sind und nicht über einen standardbranch für unbekannte Typen verfügen, können Sie einen neuen Branch hinzufügen, der den neuen Datentyp verwendet. Dadurch wird die Größe der Datenstruktur nicht geändert. Wenn Ihr Client mit einem neuen Server kommuniziert, kann er den neuen Datentyp verwenden. Wenn der Client jedoch mit einem alten Server kommuniziert, gibt die Laufzeit das \_ ungültige RPC S- \_ Tag aus \_ . Auch hier müssen Sie den Client Code so schreiben, dass diese Ausnahme entsprechend behandelt wird.

Eine DCOM-Schnittstelle wird durch ihre GUID identifiziert. In DCOM sind Schnittstellen als unveränderlich zu sehen, und Sie können Änderungen vornehmen, indem Sie eine neue Schnittstelle erstellen, die von der alten erbt. Diese Regeln stellen sicher, dass Clients und Server kompatibel bleiben.

 

 