---
title: Bereitstellen von Klasseninformationen
description: Bereitstellen von Klasseninformationen
ms.assetid: 808d9a39-4511-4aba-a23f-3c929970503b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a042283ca9ba6eb29bceeacef2c32f9bd401ef09e92eafbc737711d0d930336
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119500120"
---
# <a name="providing-class-information"></a>Bereitstellen von Klasseninformationen

Es ist häufig nützlich, wenn ein Client eines Objekts die Typinformationen des Objekts untersucht. Angesichts der CLSID des Objekts kann ein Client die Typbibliothek des Objekts mithilfe von Registrierungseinträgen suchen und dann die Typbibliothek auf den Co-Klasseneintrag in der Bibliothek überprüfen, der der CLSID entspricht.

Allerdings verfügen nicht alle Objekte über eine CLSID, obwohl sie weiterhin Typinformationen bereitstellen müssen. Darüber hinaus ist es für einen Client praktisch, ein Objekt einfach nach seinen Typinformationen zu fragen, anstatt das gesamte Tedium zu durchlaufen, um die gleichen Informationen aus Registrierungseinträgen zu extrahieren. Diese Funktion ist wichtig, wenn es um ausgehende Schnittstellen für miteinander verknüpfte Objekte geht. (Weitere Informationen dazu, wie verbindungsfähige Objekte diese Funktion bereitstellen, finden Sie unter [Verwenden von IProvideClassInfo.)](using-iprovideclassinfo.md)

In diesen Fällen kann ein Client das -Objekt nach [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) oder [**IProvideClassInfo2**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo2)abfragen. Wenn diese Schnittstellen vorhanden sind, ruft der Client die [**GetClassInfo-Methode**](/windows/desktop/api/OCIdl/nf-ocidl-iprovideclassinfo-getclassinfo) auf, um die Typinformationen für die Schnittstelle abzurufen.

Durch die Implementierung von [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) oder [**IProvideClassInfo2**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo2)gibt ein -Objekt an, dass es Typinformationen für die gesamte Klasse bereitstellen kann. das heißt, was im Co-Klassenabschnitt der Typbibliothek beschrieben wird, wenn es über eine solche verfügt. [**GetClassInfo**](/windows/desktop/api/OCIdl/nf-ocidl-iprovideclassinfo-getclassinfo) gibt einen **ITypeInfo-Zeiger** zurück, der den Co-Klasseninformationen des Objekts entspricht. Mit diesem **ITypeInfo-Zeiger** kann der Client alle definitionen der eingehenden und ausgehenden Schnittstellen des Objekts untersuchen.

Das -Objekt kann auch [**IProvideClassInfo2**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo2)bereitstellen. Die **IProvideClassInfo2-Schnittstelle** ist eine einfache Erweiterung für [**IProvideClassInfo,**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) mit der die ausgehenden Schnittstellenbezeichner eines Objekts für den Standardereignissatz schnell und einfach abgerufen werden können. **IProvideClassInfo2** wird von **IProvideClassInfo** abgeleitet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[COM-Clients und -Server](com-clients-and-servers.md)
</dt> </dl>

 

 




