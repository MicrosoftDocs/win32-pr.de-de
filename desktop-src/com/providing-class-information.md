---
title: Bereitstellen von Klassen Informationen
description: Bereitstellen von Klassen Informationen
ms.assetid: 808d9a39-4511-4aba-a23f-3c929970503b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc4505a12d4a7f50a605cbd04cae33805db2b19b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104100699"
---
# <a name="providing-class-information"></a>Bereitstellen von Klassen Informationen

Es ist häufig sinnvoll, dass ein Client eines Objekts die Typinformationen des Objekts untersucht. Aufgrund der CLSID des Objekts kann ein Client die Typbibliothek des Objekts mithilfe von Registrierungs Einträgen suchen und dann die Typbibliothek für den Co-Klassen Eintrag in der Bibliothek scannen, die der CLSID entspricht.

Allerdings haben nicht alle Objekte eine CLSID, obwohl Sie weiterhin Typinformationen bereitstellen müssen. Außerdem ist es für einen Client praktisch, eine Möglichkeit zu haben, ein Objekt einfach auf seine Typinformationen zu Fragen, anstatt alle Elemente aus Registrierungs Einträgen zu extrahieren. Diese Funktion ist wichtig, wenn Sie mit ausgehenden Schnittstellen auf Verbindungs fähigen Objekten arbeiten. (Weitere Informationen zur Bereitstellung dieser Funktion durch Verbindungs fähige Objekte finden [Sie unter Verwenden von IProvideClassInfo](using-iprovideclassinfo.md) .)

In diesen Fällen kann ein Client das Objekt für [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) oder [**IProvideClassInfo2**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo2)Abfragen. Wenn diese Schnittstellen vorhanden sind, ruft der Client die [**GetClassInfo**](/windows/desktop/api/OCIdl/nf-ocidl-iprovideclassinfo-getclassinfo) -Methode auf, um die Typinformationen für die Schnittstelle zu erhalten.

Durch die Implementierung von [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) oder [**IProvideClassInfo2**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo2)gibt ein Objekt an, dass es Typinformationen für die gesamte Klasse bereitstellen kann. Das heißt, was Sie in Ihrem Co-Klasse-Abschnitt Ihrer Typbibliothek beschreiben würde, wenn Sie eine hat. [**GetClassInfo**](/windows/desktop/api/OCIdl/nf-ocidl-iprovideclassinfo-getclassinfo) gibt einen **ITypeInfo** -Zeiger zurück, der den Co-Klasse-Informationen des Objekts entspricht. Mithilfe dieses **ITypeInfo** -Zeigers kann der Client alle eingehenden und ausgehenden Schnittstellendefinitionen des Objekts überprüfen.

Das-Objekt kann auch [**IProvideClassInfo2**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo2)bereitstellen. Die **IProvideClassInfo2** -Schnittstelle ist eine einfache Erweiterung von [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) , mit der die ausgehenden Schnittstellen Bezeichner eines Objekts für den Standard Ereignis Satz schnell und einfach abgerufen werden können. **IProvideClassInfo2** wird von **IProvideClassInfo** abgeleitet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[COM-Clients und-Server](com-clients-and-servers.md)
</dt> </dl>

 

 




