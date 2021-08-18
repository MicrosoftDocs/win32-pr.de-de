---
title: Lösung von Funktions-/Eigenschaftsnamenkonflikten in Automation in Erweiterungen
description: In diesem Thema\ 0034;Object \ 0034; gibt das Objekt als Ganzes an, wenn es von einem ADSI-Client angezeigt wird. Das heißt, ADSI und alle erweiterungen.
ms.assetid: 76207326-879e-408b-8004-06d940401a41
ms.tgt_platform: multiple
keywords:
- Lösung von Funktions- und Eigenschaftsnamenkonflikten in Automation in Erweiterungen
- extensions ADSI , Auflösen von Funktions- und Eigenschaftsnamenskonflikten in Automation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53701c95672fe209cb57a15e3292e1269dc37e66e36f041110dd502f8a8a1486
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119637540"
---
# <a name="resolution-of-functionproperty-name-conflicts-in-automation-in-extensions"></a>Lösung von Funktions-/Eigenschaftsnamenkonflikten in Automation in Erweiterungen

In diesem Thema gibt "object" das Objekt als Ganzes an, während es von einem ADSI-Client angezeigt wird. Das heißt, ADSI und alle erweiterungen.

## <a name="same-function-name-with-the-same-parameters"></a>Gleicher Funktionsname mit den gleichen Parametern

Wenn zwei oder mehr duale [**IDispatch-Schnittstellen**](/windows/win32/api/oaidl/nn-oaidl-idispatch) in einem -Objekt eine Eigenschaft oder Methode mit demselben Namen unterstützen, z. B. **Func1,** wird der Aufruf anhand der folgenden Kriterien bestimmt. Wenn der Client über einen Zeiger auf eine der dualen Schnittstellen verfügt, die eine Methode namens **Func1** unterstützen, und die Automation-Umgebung vtable-Zugriff unterstützt, wird **Func1** direkt über adsi vtable access aufgerufen.

Wenn eine der oben genannten Bedingungen false ist, werden [**IDispatch::GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames) und [**IDispatch::Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) aufgerufen, um **Func1 aufrufen.**

Weitere Informationen und eine kurze Erläuterung dazu, wie ein Client einen Zeiger auf eine duale Schnittstelle hinzufügen kann, sowie eine Beschreibung der Arten von Umgebungen, die vtable-Zugriff unterstützen, finden Sie unter Späte Bindung und [Vtable-Zugriff im ADSI-Erweiterungsmodell](late-binding-vs--vtable-access-in-the-adsi-extension-model.md).

Da alle Erweiterungsobjekte die [**IDispatch-Funktionen**](/windows/win32/api/oaidl/nn-oaidl-idispatch) zurück an den Aggregator umleiten, steuert der Aggregator, welcher **Func1** aufgerufen wird. Die Regeln sind:

-   Wenn eine Schnittstelle, die im Aggregator (ADSI) nur eine beliebige Schnittstelle unterstützt, eine Funktion namens **Func1** unterstützt, ruft der Aggregator seine eigene **Func1 auf.**
-   Andernfalls durchläuft der Aggregator jede seiner Erweiterungen in der reihenfolge, die in der Registrierung aufgeführt ist, und sucht die erste Erweiterung, die eine Funktion namens **Func1 implementiert.** Es ist möglich, aber unwahrscheinlich, dass mehrere duale [**IDispatch-Schnittstellen**](/windows/win32/api/oaidl/nn-oaidl-idispatch) in dieser ersten Erweiterung über eine Funktion namens **Func1 verfügen.** Die Erweiterung muss bestimmen, **welche Func1** in Automation immer aufgerufen werden soll.

## <a name="same-function-name-with-different-parameters"></a>Gleicher Funktionsname mit unterschiedlichen Parametern

Im vorherigen Abschnitt wurde erläutert, wie Funktionsnamenkonflikte gelöst werden können, d. &a. Funktionsnamen, die denselben Funktionsnamen und dieselbe Parameterliste haben, z. B. Zahl, Typ und Reihenfolge, wenn sie in Automation auftreten. Was passiert, wenn zwei Funktionen denselben Namen, aber unterschiedliche Parameter haben? Wenn ein ADSI-Client die Funktion mithilfe von [**IDispatch::GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames) aufruft, ohne mehrere Namen zum Angeben der Parameter zu verwenden, kann das ADSI-Erweiterungsmodell die Funktionen nicht mehrdeutigen. Basierend auf dem oben beschriebenen Auflösungsschema wird für die erste Erweiterung in der Registrierung, die diese Funktion über eine ihrer Schnittstellen unterstützt, die Version dieser Funktion aufgerufen, und der Aufruf kann fehlschlagen oder falsche Ergebnisse liefern.

Beispiel:

-   Extn1 (zuerst in der Registrierung unter der Klasse CA – höhere Priorität) unterstützt **IInterface1.**
-   Extn2 (drittes in der Registrierung unter der Klasse CA – niedrigere Priorität) unterstützt **IInterface2**.
-   **IInterface1 unterstützt** **Method1(int param1, int param2).**
-   **IInterface2 unterstützt** **Method1(int param1)**.

Ein ADSI-Client verfügt über einen [**IDispatch-Schnittstellenzeiger**](/windows/win32/api/oaidl/nn-oaidl-idispatch) auf ein Objekt der Klasse CA. Sie möchte **IInterface2::Method1 aufrufen.** Wenn der Client "pDispatch->GetIDsOfNames(IID \_ NULL, rgszNames, 1, MY LCID, rgDispId)" aufruft, indem nur der Funktionsname \_ "Method1" in *rgszNames \[ 0 \]* gespeichert wird, wird **IInterface1::Method1** anstelle der gewünschten **IInterface2::Method1** aufgerufen, und die Funktion schlägt fehl, da die Anzahl der Parameter unterschiedlich ist.

Um dieses Problem zu minimieren, können Erweiterungsentwickler ihren Funktionsnamen ihre eigenen spezifischen Bezeichner voran stellen und Schnittstellenentwürfe vermeiden, die Funktionen desselben Namens, aber unterschiedliche Parameter verwenden.

Wenn ein Namenskonflikt auftritt, können ADSI-Clients das Problem durch direkten vtable-Zugriff vermeiden, wenn es sich bei der Schnittstelle um eine duale Schnittstelle handelt. Wenn kein direkter vtable-Zugriff möglich ist, sollten ADSI-Clients [**IDispatch::GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames) mit mehreren Namen aufrufen und dabei die Funktionsnamen sowie die Parameter im zuvor beschriebenen *Array rgszNames* angeben.

Visual Basic 5 die [**IDispatch::GetIDsOfNames-Funktion**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames) mit mehreren Namen nicht aufruft. Das heißt, es wird nur der Funktionsname an **GetIDsOfNames** übergeben, aber keine Argumente. In Visual Basic 5 können Benutzer jedoch eine Funktion über direkten vtable-Zugriff aufrufen, anstatt die **IDispatch::GetIDsOfNames-Funktion** auf aufruft, wenn es sich bei der Schnittstelle um eine duale Schnittstelle handelt. Entwickler sollten nach Möglichkeit direkten vtable-Zugriff verwenden.

Weitere Informationen zur Namenskonfliktlösung finden Sie unter [Beispiel für das Auflösen von Funktionsnamenkonflikten.](example-for-resolving-function-name-conflicts.md)

 

 