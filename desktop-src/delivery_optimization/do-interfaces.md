---
title: Do-Schnittstellen
description: Verwenden Sie die folgenden Schnittstellen zur Übermittlungs Optimierung, um Dateien zu übertragen und Aufträge innerhalb der Übertragungs Warteschlange zu überwachen.
ms.assetid: 20203CCD-86CC-4551-BA4F-0A5999F8C956
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0359328f189c1a5b5d9649d8300dc59a80df4480
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106339494"
---
# <a name="do-interfaces"></a>Do-Schnittstellen

Verwenden Sie die folgenden Schnittstellen zur Übermittlungs Optimierung, um Dateien zu übertragen und Aufträge innerhalb der Übertragungs Warteschlange zu überwachen.

| Schnittstelle | BESCHREIBUNG |
|-|-|
| [**Ibackgroundcopycallback**](ibackgroundcopycallback.md) | Clients implementieren die [**ibackgroundcopycallback**](ibackgroundcopycallback.md) -Schnittstelle, um eine Benachrichtigung zu erhalten, dass ein Auftrag abgeschlossen, geändert oder fehlerhaft ist. |
| [**Ibackgroundcopyerror**](ibackgroundcopyerror.md) | Ruft die Details eines Auftrags Fehlers ab. |
| [**Ibackgroundcopyfile**](ibackgroundcopyfile.md) | Ruft die lokalen und Remote Dateinamen einer Datei Übertragungs Anforderung im Auftrag und ihren Fortschritt ab. |
| [**IBackgroundCopyFile2**](ibackgroundcopyfile2.md) | Gibt einen neuen Remote Namen für die Datei an und ruft die Liste der herunter zuladenden Bereiche ab. |
| [**IBackgroundCopyFile5**](ibackgroundcopyfile5.md) | Stellt generische Eigenschaften get-und Set-Methoden für backgroundcopyfile-Eigenschaften bereit. |
| [**IBackgroundCopyJob**](ibackgroundcopyjob-.md) | Fügt dem Auftrag Dateien hinzu, legt die Prioritätsstufe des Auftrags fest, bestimmt den Status des Auftrags und startet und beendet den Auftrag. |
| [**IBackgroundCopyJob5**](ibackgroundcopyjob5.md) | Fragt mehrere optionale Verhalten eines Auftrags ab oder legt diese fest. |
| [**Ibackgroundcopymanager**](ibackgroundcopymanager.md) | Erstellt Übertragungs Aufträge, Ruft ein Enumeratorobjekt von Aufträgen in der Warteschlange ab und ruft einzelne Aufträge aus der Warteschlange ab. |
| [**Ideliveryoptimizationjob**](ideliveryoptimizationjob.md) | Verwenden Sie, um Bereiche einer Datei herunterzuladen. |
| [**Ideliveryoptimizationfile**](ideliveryoptimizationfile.md) | Verwenden Sie, um den Status einer bestimmten Datei zu identifizieren. |
| [**Idodownload**](./do/nn-do-idodownload.md) | Wird verwendet, um einen Download zu starten und zu verwalten. |
| [**Idodownloadinternal**](./dodownloadinternal/nn-dodownloadinternal-idodownloadinternal.md) | Wird verwendet, um Erweiterte Download Eigenschaften zu erhalten oder festzulegen. |
| [**Idodownloadstatus Callback**](./do/nn-do-idodownloadstatuscallback.md) | Wird zum Empfangen von Benachrichtigungen zu einem Download verwendet. |
| [**Idomanager**](./do/nn-do-idomanager.md) | Wird verwendet, um einen neuen Download zu erstellen und vorhandene Downloads aufzulisten. |
| [**Ienumbackgroundcopyfiles**](ienumbackgroundcopyfiles-.md) | Listet die Dateien im Auftrag auf. |