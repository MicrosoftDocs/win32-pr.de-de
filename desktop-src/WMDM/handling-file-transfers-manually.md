---
title: Manuelles Verarbeiten von Dateiübertragungen
description: Manuelles Verarbeiten von Dateiübertragungen
ms.assetid: ff94191b-a0f2-4118-996c-d040f214fb9b
keywords:
- Windows Media Device Manager, manuelle Dateiübertragungen
- Device Manager, manuelle Dateiübertragungen
- Programmier Handbuch, manuelle Dateiübertragungen
- Desktop Anwendungen, manuelle Dateiübertragungen
- Erstellen von Windows Media Device Manager-Anwendungen, manuelle Dateiübertragungen
- manuelle Dateiübertragungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2bf12404e8cd83b6f0c0e4f1c8ec8b0b7bda205
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728937"
---
# <a name="handling-file-transfers-manually"></a>Manuelles Verarbeiten von Dateiübertragungen

Die Anwendung kann die [**iwmdmoperation**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation) -Schnittstelle implementieren, um einen Teil des Lese-oder Schreibvorgangs zu verwalten. Bei einem Lesevorgang von einem Gerät ermöglicht die-Implementierung der Anwendung den Empfang von Blöcken von Rohdaten aus einer Gerätedatei. Auf einem Schreibzugriff auf ein Gerät ermöglicht es der Anwendung, Blöcke von Rohdaten an eine Datei auf dem Gerät zu senden.

Bei Lese-und Schreibvorgängen übergibt die [**iwmdmoperation:: transferobjectdata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-transferobjectdata) -Methode die Daten zwischen dem Computer und dem Gerät. Um die Richtung der Datenübertragung zu erkennen, muss Ihre Anwendung ein Flag festlegen, wenn Windows Media Device Manager [**BeginRead**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-beginread) oder [**BeginWrite**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-beginwrite)aufruft. Wenn die [**End**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-end) -Methode aufgerufen wird, sollte die Anwendung dieses Flag zurücksetzen.

> [!Note]  
> Wenn der Dienstanbieter und das Gerät [**IMDSPObject2**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspobject2)ordnungsgemäß implementieren, wird zuerst die [IWMDMOperation3:: transferobjectdataonclearchannel](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation3-transferobjectdataonclearchannel) -Methode der Anwendung aufgerufen, sofern diese implementiert ist. Diese Methode ist eine effizientere Methode zum Übertragen von Daten. **Transferobjectdataonclearchannel** wird auf die gleiche Weise wie **transferobjectdata** behandelt, mit dem Unterschied, dass die Daten niemals verschlüsselt werden und keine Mac-Werte zur Überprüfung verwendet werden.

 

In den folgenden Abschnitten werden sowohl der Lesevorgang als auch der Schreibvorgang beschrieben, wenn die Anwendung **iwmdmoperation** implementiert.

**Lesen von einem Gerät**

Beim Lesen einer Datei von einem Gerät ruft Windows Media Device Manager die folgenden **iwmdmoperation** -Methoden in der angegebenen Reihenfolge auf:

-   [**BeginRead**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-beginread) Wird aufgerufen, um die Anwendung darüber zu benachrichtigen, dass ein Lesevorgang vom Gerät gestartet wird.
-   [**Transferobjectdata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-transferobjectdata) Wird einmal oder mehrmals aufgerufen. Die Verarbeitung von Daten wird in den folgenden Schritten beschrieben:
    1.  **Transferobjectdata** empfängt einen Puffer, *pData*, Größe von *pdwSize* (Bytes), gefüllt mit Daten und einen Mac zum Überprüfen der eingehenden Daten.
    2.  Die Anwendung überprüft die eingehenden Parameter mit dem eingehenden Daten-Mac.
    3.  Die Anwendung entschlüsselt und liest so viele Daten wie möglich in *pData* und ändert den zurückgegebenen Wert von " *pdwSize* ", um anzugeben, wie viele Bytes tatsächlich gelesen wurden.
    4.  Die Anwendung entschlüsselt die Daten mithilfe von [**csecurechannelclient::D ecryptparam**](/previous-versions/bb231586(v=vs.85)), speichert Sie oder verwendet Sie nach Bedarf.
    5.  **Transferobjectdata** gibt S \_ OK zurück.
    6.  Windows Media Device Manager ruft **transferobjectdata** weiterhin auf, bis die Anwendung alle Daten aus der Datei gelesen hat, oder die Anwendung gibt zurück, dass der WMDM E-Benutzer abgebrochen wurde, \_ \_ \_ um den Vorgang abzubrechen (in diesem Fall wird der Lesevorgang abgebrochen, und Windows Media Device Manager-Aufrufe **enden**).
-   [**Ende**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-end) Wird aufgerufen, um die Anwendung zu benachrichtigen, dass ein Lesevorgang von einem Gerät beendet wird.

**Schreiben auf ein Gerät**

Wenn Sie eine Datei auf das Gerät schreiben, ruft Windows Media Device Manager die folgenden **iwmdmoperation** -Methoden in der angegebenen Reihenfolge auf:

-   [**Getobjectname**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-getobjectname) Wird aufgerufen, um der Anwendung das Angeben eines Namens für den neuen Speicher zu ermöglichen. Diese Methode wird nur aufgerufen, wenn die Anwendung keinen Namen in der **Insert** -Methode angegeben hat.
-   [**Getobjectattributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-getobjectattributes) Wird aufgerufen, damit die Anwendung Attribute für den neuen Speicher auf dem Gerät angeben kann.
-   [**BeginWrite**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-beginwrite) Wird aufgerufen, um zu benachrichtigen, dass ein Schreibvorgang auf das Gerät beginnt.
-   [**Getobjecttotalsize**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-getobjecttotalsize) Wird aufgerufen, um die Gesamtgröße des Objekts abzurufen, das auf das Gerät geschrieben wird, um die Optimierung der Übertragung zu ermöglichen und Windows Media Device Manager die Möglichkeit zu geben, die Übertragung abzubrechen, wenn die Datei für das Gerät zu groß ist.
-   [**Transferobjectdata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-transferobjectdata) Wird einmal oder mehrmals aufgerufen. Die Verarbeitung von Daten wird in den folgenden Schritten beschrieben:
    1.  **Transferobjectdata** erhält einen Zeiger auf einen Puffer mit einer Größe von *pdwSize* -bytes.
    2.  Die Anwendung ruft einen Datenblock ab, der an das Gerät gesendet werden soll, in der Regel durchlesen von Daten aus einer Datei und füllt den empfangenen Puffer mit bis zu *pdwSize* -Bytes aus. Sie sollte *pdwSize* (falls erforderlich) ändern, um widerzuspiegeln, wie viele Bytes dem Puffer hinzugefügt wurden.
    3.  Die Anwendung erstellt einen Mac aller Methoden Parameter.
    4.  Die Anwendung verschlüsselt die Daten im Puffer mithilfe von [**csecurechannelclient:: verschlüsseltparam**](/previous-versions/bb231587(v=vs.85)).
    5.  **Transferobjectdata** gibt s \_ OK zurück, um anzugeben, dass mehr Daten vorhanden sind, oder s \_ false, um anzugeben, dass keine Daten mehr vorhanden sind. Wenn die Anwendung den WMDM \_ E \_ \_ -Benutzer abgebrochen zurückgibt, wird der Schreibvorgang abgebrochen, und Windows Media Device Manager ruft **End** auf.
    6.  Windows Media Device Manager setzt das Abrufen von **transferobjectdata** fort, solange die Anwendung S \_ OK zurückgibt.
-   [**Ende**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-end) Wird aufgerufen, um zu benachrichtigen, dass ein Schreibvorgang auf das Gerät endet.

Ein Codebeispiel finden Sie unter [Verschlüsselung und Entschlüsselung](encryption-and-decryption.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Erstellen einer Windows Media Device Manager-Anwendung**](creating-a-windows-media-device-manager-application.md)
</dt> </dl>

 

 