---
title: Auflösung von Funktions-/Eigenschaftennamen-Konflikten bei der Automatisierung in Erweiterungen
description: 'In diesem Thema: \ 0034; Object \ 0034; Gibt das-Objekt als Ganzes als ADSI-Client an. Das heißt, ADSI und alle zugehörigen Erweiterungen.'
ms.assetid: 76207326-879e-408b-8004-06d940401a41
ms.tgt_platform: multiple
keywords:
- Auflösung von Funktions-und Eigenschafts Namenskonflikten bei der Automatisierung in Erweiterungen
- Erweiterungen ADSI, Auflösen von Funktions-und Eigenschafts Namenskonflikten in Automation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9a7ac99b99ecdf0ee1b940f066d9e8166a15542
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104391009"
---
# <a name="resolution-of-functionproperty-name-conflicts-in-automation-in-extensions"></a>Auflösung von Funktions-/Eigenschaftennamen-Konflikten bei der Automatisierung in Erweiterungen

In diesem Thema zeigt "Object" das Objekt als Ganzes als ADSI-Client an. Das heißt, ADSI und alle zugehörigen Erweiterungen.

## <a name="same-function-name-with-the-same-parameters"></a>Gleicher Funktions Name mit denselben Parametern

Wenn zwei oder mehr Dual- [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstellen in einem Objekt eine Eigenschaft oder Methode mit demselben Namen unterstützen, z. b. **func1**, wird der Aufruf anhand der folgenden Kriterien festgelegt. Wenn der Client über einen Zeiger auf eine der Dual-Schnittstellen verfügt, die eine Methode mit dem Namen **func1** unterstützen, und wenn die Automatisierungs Umgebung Vtable-Zugriff unterstützt, wird **func1** direkt über den ADSI Vtable-Zugriff aufgerufen.

Wenn eine der oben genannten Bedingungen false ist, werden [**IDispatch:: GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames) und [**IDispatch:: Aufrufen**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) aufgerufen, um **func1** aufzurufen.

Weitere Informationen und eine kurze Erläuterung darüber, wie ein Client einen Zeiger auf eine duale Schnittstelle und eine Beschreibung der Typen von Umgebungen, die den vtable-Zugriff unterstützen, hinzufügen können, finden Sie unter [späte Bindung im Vergleich zu Vtable-Zugriff im ADSI-Erweiterungs Modell](late-binding-vs--vtable-access-in-the-adsi-extension-model.md).

Da alle Erweiterungs Objekte die [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Funktionen zurück an den Aggregator umleiten, steuert der Aggregator, welche **func1** aufgerufen wird. Die Regeln lauten wie folgt:

-   Wenn eine beliebige Schnittstelle vorhanden ist, und wenn eine beliebige Schnittstelle vorhanden ist, unterstützt der Aggregator im Aggregator (ADSI) eine Funktion mit dem Namen **func1**, ruft der Aggregator seinen eigenen **func1** auf.
-   Andernfalls durchläuft der Aggregator alle seine Erweiterungen in der Reihenfolge, die in der Registrierung aufgeführt ist, und sucht die erste Erweiterung, die eine Funktion mit dem Namen **func1** implementiert. Es ist möglich, aber unwahrscheinlich, dass mehrere Dual- [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstellen in dieser ersten Erweiterung eine Funktion mit dem Namen **func1** haben. Die Erweiterung muss bestimmen, welche **func1** immer in Automation aufgerufen werden soll.

## <a name="same-function-name-with-different-parameters"></a>Gleicher Funktions Name mit unterschiedlichen Parametern

Im vorherigen Abschnitt wurde erläutert, wie Funktionsnamen Konflikte aufgelöst werden, d. h. Funktionsnamen, die den gleichen Funktionsnamen und die gleiche Parameterliste aufweisen, wie z. b. Anzahl, Typ und Reihenfolge, wenn Sie in Automation auftritt. Was geschieht, wenn zwei Funktionen denselben Namen, aber unterschiedliche Parameter aufweisen? Wenn ein ADSI-Client die Funktion mithilfe von [**IDispatch:: GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames) aufruft, ohne mehrere Namen zum Angeben der Parameter zu verwenden, kann das ADSI-Erweiterungs Modell die Funktionen nicht unterscheiden. Basierend auf dem oben beschriebenen Auflösungs Schema ist die erste Erweiterung in der Registrierung, die diese Funktion über eine der Schnittstellen unterstützt, Ihre Version dieser Funktion wird aufgerufen, und der Aufruf schlägt möglicherweise fehl oder liefert falsche Ergebnisse.

Beispiel:

-   Extn1 (First in der Registrierung unter der Klasse ca – höhere Priorität) unterstützt **IInterface1**.
-   Extn2 (drittes in der Registrierung unter Class ca – niedrigere Priorität) unterstützt **IInterface2**.
-   **IInterface1** unterstützt **Methode1 (int param1, int param2)**.
-   **IInterface2** unterstützt **Methode1 (int Param1)**.

Ein ADSI-Client verfügt über einen [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstellen Zeiger auf ein Objekt der Klasse ca. Er möchte **IInterface2:: Methode1** aufrufen. Wenn der Client "pdispatch->GetIDsOfNames (IID null) aufruft \_ , rgsznames, 1, My \_ LCID, rgdispid)" durch einfaches Speichern des Funktionsnamens "Methode1" in *rgsznames \[ 0 \]*, dann **IInterface1:: Methode1** anstelle der gewünschten **IInterface2:: Methode1** wird aufgerufen, und die Funktion schlägt fehl, da die Anzahl der Parameter unterschiedlich ist.

Um dieses Problem zu minimieren, können Erweiterungs Entwickler ihre Funktionsnamen mit ihren eigenen spezifischen bezeichtern versehen und Schnittstellen Entwürfe vermeiden, die Funktionen mit dem gleichen Namen, aber unterschiedlichen Parametern verwenden.

Wenn ein namens Konflikt auftritt, können ADSI-Clients das Problem durch direkten Vtable-Zugriff vermeiden, wenn es sich bei der Schnittstelle um eine duale Schnittstelle handelt. Wenn kein direkter Vtable-Zugriff möglich ist, sollten ADSI-Clients [**IDispatch:: GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames) mit mehreren Namen aufrufen und dabei die Funktionsnamen sowie die Parameter in dem zuvor beschriebenen Array *rgsznames* angeben.

In Visual Basic 5 wird die [**IDispatch:: GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames) -Funktion nicht mit mehreren Namen aufgerufen. Das heißt, es übergibt nur den Funktionsnamen an **GetIDsOfNames**, aber keine Argumente. Allerdings ermöglicht Visual Basic 5 Benutzern, eine Funktion durch direkten Vtable-Zugriff aufzurufen, anstatt die Funktion **IDispatch:: GetIDsOfNames** aufzurufen, wenn die Schnittstelle eine duale Schnittstelle ist. Entwickler sollten, sofern möglich, direkten Vtable-Zugriff verwenden.

Weitere Informationen zur Auflösung von Namenskonflikten finden Sie unter [Beispiel für das Auflösen von Funktionsnamen Konflikten](example-for-resolving-function-name-conflicts.md).

 

 