---
title: Verwenden von IProvideClassInfo
description: Verwenden von IProvideClassInfo
ms.assetid: 16541aab-474f-4ae5-a6b6-fb2fea6d38ab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32a3abd61bb330a2a7d681b6d53648c5fbde8c53
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104039679"
---
# <a name="using-iprovideclassinfo"></a>Verwenden von IProvideClassInfo

Ein Verbindungs fähigen-Objekt kann die [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) -Schnittstelle und die [**IProvideClassInfo2**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo2) -Schnittstelle anbieten, damit Ihre Clients ihre Typinformationen problemlos überprüfen können. Diese Funktion ist wichtig beim Umgang mit ausgehenden Schnittstellen, die definitionsgemäß durch ein Objekt definiert, aber von einem Client auf einem eigenen Sink-Objekt implementiert werden. In einigen Fällen ist eine ausgehende Schnittstelle zum Zeitpunkt der Kompilierung sowohl dem Verbindungs fähigen-Objekt als auch dem sink-Objekt bekannt. Dies ist der Fall bei [**IPropertyNotifySink**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertynotifysink).

In anderen Fällen kennt jedoch nur das Verbindungs fähige Objekt seine ausgehenden Schnittstellendefinitionen zur Kompilierzeit. In diesen Fällen muss der Client die Typinformationen für die ausgehende Schnittstelle abrufen, damit eine Senke, die die richtigen Einstiegspunkte unterstützt, dynamisch bereitgestellt werden kann, wie im folgenden dargestellt:

1.  Der Client listet die Verbindungspunkte auf und ruft dann die IIDs der ausgehenden Schnittstellen ab, die vom Verbindungs fähigen-Objekt unterstützt werden, und ruft für jeden Verbindungspunkt [**IConnectionPoint:: GetConnectionInterface**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-getconnectioninterface) auf.
2.  Der Client fragt das Verbindungs fähige Objekt für eine der [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) -Schnittstellen ab.
3.  Der Client ruft Methoden in der [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) -Schnittstelle auf, um die Typinformationen für die ausgehende Schnittstelle zu erhalten.
4.  Der Client erstellt ein Sink-Objekt, das die Ausgangs Schnittstelle unterstützt.
5.  Der Prozess wird fortgesetzt, und der Client ruft [**IConnectionPoint:: Empfehlung**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-advise) auf, um seine Senke mit dem Verbindungspunkt zu verbinden.

In den Typinformationen markiert die Attribut [**Quelle**](/windows/desktop/Midl/source) eine [**Schnittstelle**](/windows/desktop/Midl/interface) oder eine [**dispinterface**](/windows/desktop/Midl/dispinterface) , die unter einer [**Co-Klasse**](/windows/desktop/Midl/coclass) als ausgehende Schnittstelle aufgeführt ist. Die ohne dieses Attribut aufgelisteten werden als eingehende Schnittstellen betrachtet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verbindungs fähige Objekt Schnittstellen](connectable-object-interfaces.md)
</dt> <dt>

[Bereitstellen von Klassen Informationen](providing-class-information.md)
</dt> </dl>

 

 