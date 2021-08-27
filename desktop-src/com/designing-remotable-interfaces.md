---
title: Entwerfen von remotable-Schnittstellen
description: Mit der Einführung des verteilten Komponentenobjektmodells ist es wichtig, dass Ihre benutzerdefinierte Schnittstelle remotable ist, auch wenn Sie sie nur in Der Prozess verwenden möchten.
ms.assetid: 2ee4d950-dfd5-4965-bd77-a600e878be59
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52df6deb3f83f253fc46436ba992dc3fc10f74d84e43c6027fd4426b3171a838
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120071000"
---
# <a name="designing-remotable-interfaces"></a>Entwerfen von remotable-Schnittstellen

Mit der Einführung des verteilten Komponentenobjektmodells ist es wichtig, dass Ihre benutzerdefinierte Schnittstelle remotable ist, auch wenn Sie sie nur in Der Prozess verwenden möchten.

MIDL ist mehr als nur eine Möglichkeit, Headerdateien für Ihre Schnittstellen zu generieren. Es ist eine Programmiersprache für Remoting, mit der Sie Ihre Schnittstellen über Computer-, Prozess- und Threadgrenzen hinweg verwenden können. Dies bedeutet, dass Sie das Verhalten Ihrer MIDL-definierten Schnittstellen unter diesen Bedingungen überprüfen müssen, bevor Sie Ihr Programm für Kunden veröffentlichen. Wenn Sie einen Fehler in Ihrer IDL gemacht haben und die Schnittstelle nicht ordnungsgemäß entfernt wird, kann es schwierig sein, diesen Fehler zu beheben. Entweder müssen Sie die Schnittstelle mit einer neuen IID überarbeiten und die alte schnittstelle aus Gründen der Abwärtskompatibilität in lassen, oder Sie müssen jeden Client und jeden Servercomputer überall gleichzeitig konvertieren.

Auch wenn Ihre Schnittstelle nie prozessintern verwendet wird, kann sie threadübergreifend verwendet werden. Das schlechteste Problem für eine nicht überprüfte IDL-Datei kann für Prozessserver auftreten, die nicht mehrere [Singlethread-Apartment unterstützen).](single-threaded-apartments.md) Ein Server, auf dem kein Threadingmodell angegeben ist, ist implizit ein Singlethreading. Alles, was als Singlethreading gekennzeichnet ist, wird auf den Thread erzwungen, der zuerst [**CoInitialize**](/windows/desktop/api/Objbase/nf-objbase-coinitialize) oder [**CoInitializeEx genannt hat.**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) Wenn ein anderer Thread das Objekt aktiviert hat, müssen alle Schnittstellen auf diesem Singlethreadserver an den aktivierenden Thread zurückverleitet werden, was als Reaktion auf einen Aufruf von QueryInterface zu einer Rückgabe von REGDB \_ E \_ IIDNOTREG führen [**kann.**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) Sofern Sie nicht unbedingt sicher sein können, dass Ihre Schnittstelle sowohl in Bearbeitung ist als auch immer im selben Thread aufgerufen wird, werden Sie zu einem bestimmten Zeitpunkt remote enfernt.

Schließlich müssen Sie als Schnittstellen-Designer überlegen, wie Clientanwendungen Ihre Schnittstelle verwenden. Zwei Dinge bestimmen zusammen, ob eine Schnittstelle über Prozess- und Computergrenzen hinweg effizient ist: die Häufigkeit von Methodenaufrufen über die Schnittstellengrenze hinweg und die Menge an Daten, die in einem bestimmten Methodenaufruf übertragen werden sollen. Obwohl COM prozess- und netzwerkübergreifende Aufrufe für Programme transparent macht, können Aufrufe mit hoher Frequenz und hoher Bandbreite nicht über Adressräume hinweg effizient sein. In einigen Fällen ist es besser, Schnittstellen zu entwerfen, die normalerweise nur als Prozessserver implementiert werden, während andere Schnittstellen für die Remotenutzung besser geeignet sind.

 

 




