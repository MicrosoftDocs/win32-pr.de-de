---
title: Implementieren der Verweiszählung
description: Implementieren der Verweiszählung
ms.assetid: d4fd98c9-afa4-4c5c-a3c9-44d34881cbdb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efa2a3e9827d35d07fa88b62c6f1097fcb3ad3ae3b5b75764deeac1c9c271050
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048158"
---
# <a name="implementing-reference-counting"></a>Implementieren der Verweiszählung

Die Verweiszählung erfordert Sowohl die Arbeit des Implementors einer Klasse als auch der Clients, die Objekte dieser Klasse verwenden. Wenn Sie eine Klasse implementieren, müssen Sie die [**Methoden AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) und [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) als Teil der [**IUnknown-Schnittstelle**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) implementieren. Diese beiden Methoden verfügen über die folgenden einfachen Implementierungen:

-   [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) erhöht die interne Verweisanzahl des Objekts.
-   [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) dekrementiert zuerst die interne Verweisanzahl des Objekts und überprüft dann, ob die Verweisanzahl auf 0 (null) gefallen ist. Wenn dies der Fall ist, bedeutet dies, dass das Objekt nicht mehr verwendet wird, sodass die **Release-Funktion** das Objekt frei macht.

Ein gängiger Implementierungsansatz für die meisten Objekte ist, dass nur eine Implementierung dieser Methoden (zusammen mit [**QueryInterface)**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q))verwendet wird, die von allen Schnittstellen gemeinsam genutzt wird, und somit eine Verweisanzahl, die für das gesamte Objekt gilt. Aus Sicht eines Clients ist die Verweiszählung jedoch streng und eindeutig ein Schnittstellenzeiger-Konzept, und daher können Objekte implementiert werden, die diese Funktion nutzen, indem sie Teile ihrer Funktionalität dynamisch erstellen, zerstören, laden oder entladen, die auf den derzeit noch verfügbaren Schnittstellenzeigern basieren. Diese werden umgangssprachlich als *Abreißschnittstellen bezeichnet.*

Wenn ein Client eine Methode (oder API-Funktion), z. B. [**QueryInterface,**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q))aufruft, die einen neuen Schnittstellenzeiger zurückgibt, ist die aufgerufene Methode dafür verantwortlich, den Verweiszähler über den zurückgegebenen Zeiger zu erhöhen. Wenn ein Client beispielsweise zum ersten Mal ein Objekt erstellt, empfängt er einen Schnittstellenzeiger auf ein Objekt, das aus Sicht des Clients einen Verweiszähler von 1 auf hat. Wenn der Client dann [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) für den Schnittstellenzeiger aufruft, wird die Verweisanzahl zu zwei. Der Client muss [**Release zweimal auf**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) dem Schnittstellenzeiger aufrufen, um alle Verweise auf das Objekt zu ablegen.

Ein Beispiel dafür, wie die Verweisanzahl ausschließlich pro Schnittstellenzeiger erfolgt, tritt auf, wenn ein Client [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) für den ersten Zeiger entweder für eine neue Schnittstelle oder dieselbe Schnittstelle aufruft. In beiden Fällen muss der Client [](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) release einmal für jeden Zeiger aufrufen. COM erfordert nicht, dass ein Objekt denselben Zeiger zurück gibt, wenn es mehrmals nach derselben Schnittstelle gefragt wird. (Die einzige Ausnahme ist eine Abfrage an [**IUnknown,**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown)die ein Objekt für COM identifiziert.) Dadurch kann die Objektimplementierung Ressourcen effizient verwalten.

Threadsicherheit ist auch ein wichtiges Problem bei der Implementierung von [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) und [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release). Weitere Informationen finden Sie unter [Prozesse, Threads und Apartment](processes--threads--and-apartments.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwalten der Objektlebensdauer durch Verweiszählung](managing-object-lifetimes-through-reference-counting.md)
</dt> </dl>

 

 