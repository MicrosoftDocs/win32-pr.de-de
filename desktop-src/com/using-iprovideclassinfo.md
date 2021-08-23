---
title: Verwenden von IProvideClassInfo
description: Verwenden von IProvideClassInfo
ms.assetid: 16541aab-474f-4ae5-a6b6-fb2fea6d38ab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c589e86596bf3e6719d3db8589570cfe347150c077e6bad19373693c18ee1ce0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118550574"
---
# <a name="using-iprovideclassinfo"></a>Verwenden von IProvideClassInfo

Ein verbindungsfähiges Objekt kann die [**Schnittstellen IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) und [**IProvideClassInfo2**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo2) anbieten, damit seine Clients seine Typinformationen leicht untersuchen können. Diese Funktion ist wichtig beim Umgang mit ausgehenden Schnittstellen, die definitionsgemäß durch ein -Objekt definiert, aber von einem Client in einem eigenen Senkenobjekt implementiert werden. In einigen Fällen ist eine ausgehende Schnittstelle zur Kompilierzeit sowohl dem verbindungsierbaren Objekt als auch dem Senkenobjekt bekannt. dies ist bei [**IPropertyNotifySink der Fall.**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertynotifysink)

In anderen Fällen kennt jedoch nur das verbindende Objekt seine ausgehenden Schnittstellendefinitionen zur Kompilierzeit. In diesen Fällen muss der Client die Typinformationen für die ausgehende Schnittstelle abrufen, damit er wie folgt dynamisch eine Senke bereitstellen kann, die die richtigen Einstiegspunkte unterstützt:

1.  Der Client listet die Verbindungspunkte auf und ruft dann für jeden Verbindungspunkt [**IConnectionPoint::GetConnectionInterface**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-getconnectioninterface) auf, um die IIDs ausgehender Schnittstellen zu erhalten, die vom verbindungsierbaren Objekt unterstützt werden.
2.  Der Client fragt das verbindungsfähige Objekt nach einer der [**IProvideClassInfo-Schnittstellen**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) ab.
3.  Der Client ruft Methoden in den [**IProvideClassInfo-Schnittstellen**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) auf, um die Typinformationen für die ausgehende Schnittstelle zu erhalten.
4.  Der Client erstellt ein Senkenobjekt, das die ausgehende Schnittstelle unterstützt.
5.  Der Prozess wird fortgesetzt, und der Client ruft [**IConnectionPoint::Advise auf,**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-advise) um seine Senke mit dem Verbindungspunkt zu verbinden.

In den Typinformationen markiert die [](/windows/desktop/Midl/interface) [**Attributquelle**](/windows/desktop/Midl/source) eine Schnittstelle [**oder Disp-Schnittstelle,**](/windows/desktop/Midl/dispinterface) die unter einer [**Co-Klasse**](/windows/desktop/Midl/coclass) als ausgehende Schnittstelle aufgeführt ist. Diejenigen, die ohne dieses Attribut aufgelistet sind, werden als eingehende Schnittstellen betrachtet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Schnittstellen für verbindende Objekte](connectable-object-interfaces.md)
</dt> <dt>

[Bereitstellen von Klasseninformationen](providing-class-information.md)
</dt> </dl>

 

 