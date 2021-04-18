---
title: Implementieren der Verweis Zählung
description: Implementieren der Verweis Zählung
ms.assetid: d4fd98c9-afa4-4c5c-a3c9-44d34881cbdb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0d4dfe2b0faf2fc6557d1b089e33ae6ce4b98cb
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "106337877"
---
# <a name="implementing-reference-counting"></a>Implementieren der Verweis Zählung

Die Verweis Zählung erfordert die Arbeit an einem Teil der Implementierung einer Klasse und den Clients, die Objekte dieser Klasse verwenden. Wenn Sie eine Klasse implementieren, müssen Sie die [**adressf**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) -und [**releasemethoden**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) als Teil der [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) -Schnittstelle implementieren. Diese beiden Methoden verfügen über die folgenden einfachen Implementierungen:

-   [**Adressf**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) Inkremente den internen Verweis Zähler des Objekts.
-   [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) Dekremente zuerst den internen Verweis Zähler des Objekts und dann überprüft, ob der Verweis Zähler auf null gefallen ist. Wenn dies der Fall ist, bedeutet dies, dass das Objekt nicht mehr verwendet wird, sodass die Freigabe Funktion das Objekt **freigibt** .

Ein gängiger Implementierungs Ansatz für die meisten Objekte besteht darin, dass nur eine Implementierung dieser Methoden (zusammen mit [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q))) vorhanden ist, die von allen Schnittstellen gemeinsam genutzt wird, und somit ein Verweis Zähler, der auf das gesamte Objekt angewendet wird. Allerdings ist die Verweis Zählung aus Sicht eines Clients streng und eindeutig ein Schnittstellen Zeiger Konzept. Daher können Objekte, die diese Funktion nutzen, durch dynamisches erstellen, zerstören, laden und Entladen von Teilen ihrer Funktionalität basierend auf den aktuell ausgewertenden Schnittstellen Zeigern implementiert werden. Diese werden als " *abtrennbare Schnittstellen*" bezeichnet.

Wenn ein Client eine Methode (oder API-Funktion) aufruft, wie z. b. [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)), die einen neuen Schnittstellen Zeiger zurückgibt, ist die aufgerufene Methode für das Inkrementieren des Verweis zähgers über den zurückgegebenen Zeiger verantwortlich. Wenn ein Client z. b. zuerst ein-Objekt erstellt, empfängt er einen Schnittstellen Zeiger auf ein Objekt, das aus Sicht des Clients einen Verweis Zähler von 1 hat. Wenn der Client dann die [**adressf**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) für den Schnittstellen Zeiger aufruft, wird der Verweis Zähler zu zwei. Der Client muss [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) zweimal für den Schnittstellen Zeiger abrufen, um alle Verweise auf das Objekt zu löschen.

Ein Beispiel dafür, wie Verweis Zähler ausschließlich pro Schnittstelle sind, tritt auf, wenn ein Client [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) für den ersten Zeiger für eine neue Schnittstelle oder die gleiche Schnittstelle aufruft. In jedem dieser Fälle ist es erforderlich, dass der Client die [**Freigabe**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) für jeden Zeiger einmal aufruft. COM erfordert nicht, dass ein Objekt denselben Zeiger zurückgibt, wenn er mehrmals zur gleichen Schnittstelle aufgefordert wird. (Die einzige Ausnahme hierbei ist eine [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown)-Abfrage, die ein Objekt für com identifiziert.) Dies ermöglicht es der Objekt Implementierung, Ressourcen effizient zu verwalten.

Thread Sicherheit ist auch ein wichtiges Problem beim Implementieren von [**Adressaten**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) und [**Releases**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release). Weitere Informationen finden Sie unter [Prozesse, Threads und Apartments](processes--threads--and-apartments.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwalten von Objekt Lebensdauern durch Verweis Zählung](managing-object-lifetimes-through-reference-counting.md)
</dt> </dl>

 

 