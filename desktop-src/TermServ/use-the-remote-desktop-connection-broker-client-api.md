---
title: Verwenden der Remotedesktopverbindung Broker-Client-API
description: Die Remotedesktopverbindung Broker-Client-API ermöglicht es Protokoll Anbietern von Drittanbietern, den Verbindungs Broker zu nutzen, um die Handhabung von Verbindungen zu beschleunigen, die das Protokoll für die Verbindung mit virtuellen Computern oder Remotedesktop Servern in einer Farm verwenden.
ms.assetid: 05C2D6CA-C9C5-4783-B196-6A02918046EF
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c931245870cfb72aed54e5aaff24e12d03ddf9e7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316185"
---
# <a name="how-to-use-the-remote-desktop-connection-broker-client-api"></a>Verwenden der Remotedesktopverbindung Broker-Client-API

Die Remotedesktopverbindung Broker-Client-API ermöglicht es Protokoll Anbietern von Drittanbietern, den Verbindungs Broker zu nutzen, um die Handhabung von Verbindungen zu beschleunigen, die das Protokoll für die Verbindung mit virtuellen Computern oder Remotedesktop Servern in einer Farm verwenden.

## <a name="instructions"></a>Anweisungen

### <a name="step-1-obtain-the-iconnectionbrokerclient-interface"></a>Schritt 1: Abrufen der iconnectionbrokerclient-Schnittstelle

Führen Sie die folgenden Schritte aus, wenn Ihre Anwendung oder Ihr Protokoll Anbieter initialisiert ist.

1.  Rufen Sie die [**cbkreateclientinstance**](cbcreateclientinstance.md) -Funktion auf, um die [**iconnectionbrokerclient**](iconnectionbrokerclient.md) -Schnittstelle abzurufen.
2.  Behalten Sie die Schnittstelle [**iconnectionbrokerclient**](iconnectionbrokerclient.md) bei, solange Sie Sie benötigen.
3.  Wenn die Schnittstelle [**iconnectionbrokerclient**](iconnectionbrokerclient.md) nicht mehr benötigt wird, können Sie die [**releasemethode**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) aufzurufen.

### <a name="step-2-request-the-target-information"></a>Schritt 2: Anfordern der Ziel Informationen

Wenn Ihr Protokoll Anbieter eine eingehende Verbindungsanforderung empfängt, führen Sie die folgenden Schritte aus, um die [**iconnectionbrokerclient:: gettargetinfo**](iconnectionbrokerclient-gettargetinfo.md) -Methode aufzurufen. Diese Methode ruft aus dem Verbindungs Broker den entsprechenden Server ab, um die Verbindung zu umzuleiten.

1.  Erstellen Sie ein Ereignis, das mithilfe der Funktion " [**kreateevent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa)" oder einer ähnlichen Funktion signalisiert werden kann, um Sie für den *hstatus usevent* -Parameter zu verwenden.
2.  Zuweisen von Arbeitsspeicher für die Parameter *ptargetinfo* und *pResult* . Diese Speicherblöcke müssen beibehalten werden, bis die gesamte Sequenz vollständig ist.
3.  Füllen Sie eine [**CB \_ - \_ Verbindungs**](cb-connection-info.md) Informationsstruktur aus, die alle Informationen über die eingehende Verbindung enthält.
4.  Nennen Sie die [**gettargetinfo**](iconnectionbrokerclient-gettargetinfo.md) -Methode, und übergeben Sie alle erforderlichen Parameter. Dabei handelt es sich um eine asynchrone Methode, die eine Instanz der [**iconnectionbrokerrequest**](iconnectionbrokerrequest.md) -Schnittstelle zurückgibt.
5.  Warten Sie, bis das *hstatus usevent* -Ereignis festgelegt wird.
6.  Wenn das *hstatusevent* -Ereignis festgelegt ist, müssen Sie die [**iconnectionbrokerrequest:: CheckStatus**](iconnectionbrokerrequest-checkstatus.md) -Methode aufrufen, um den Status der Anforderung zu bestimmen.
7.  Wenn von [**CheckStatus**](iconnectionbrokerrequest-checkstatus.md) die **\_ Status \_ Anforderung \_ "CB**" zurückgegeben wird, enthalten die Parameter *ptargetinfo* und *pResult* Ihre Informationen. Sie können die Warteschleife abbrechen, da der *hstatus usevent* -Parameter nicht mehr verwendet wird.
8.  Verwenden Sie die Informationen in der [**CB- \_ Ziel \_**](cb-target-info.md) Informationsstruktur, die vom *ptargetinfo* -Parameter dargestellt wird, um zu bestimmen, wohin die eingehende Verbindung umgeleitet werden soll.
9.  Geben Sie die [**iconnectionbrokerrequest**](iconnectionbrokerrequest.md) -Schnittstelle frei.
10. Schließen Sie das *hstatus usevent* -Ereignis handle, oder können Sie es für nachfolgende Verbindungsanforderungen wieder verwenden.

 

 