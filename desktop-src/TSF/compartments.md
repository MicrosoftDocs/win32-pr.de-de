---
title: Fer
description: Fer
ms.assetid: 7bffab6f-be40-4d3a-9342-6f81557a9656
keywords:
- Text Dienst Framework (TSF), Depots
- TSF (Text Dienst Framework), Depots
- Text Dienste, Depots
- TSF-aktivierte Anwendungen, Depots
- fer
- Text Dienst Framework (TSF), Depot-Typen
- TSF (Text Dienst Framework), Depot-Typen
- Text Dienste, Depot-Typen
- TSF-aktivierte Anwendungen, Depot Typen
- Depot Typen
- Text Dienst Framework (TSF), Depot Änderungs Benachrichtigungen
- TSF (Text Services Framework), Depot Änderungs Benachrichtigungen
- Text Dienste, Depot Änderungs Benachrichtigungen
- TSF-aktivierte Anwendungen, Depot Änderungs Benachrichtigungen
- Depot Änderungs Benachrichtigungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76636c684ee74f7e452b5602ebfd59d6d1947b0f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206514"
---
# <a name="compartments"></a>Fer

## <a name="compartment-types"></a>Depot Typen

Es gibt mehrere verschiedene Arten von Depots. Es gibt ein globales Depot, und jeder Thread-Manager, Dokument-Manager und Kontext kann ein Depot enthalten.

Mit dem globalen Depot können Clients Daten Prozess übergreifend freigeben. Rufen Sie zum Abrufen des globalen Depot-Managers [**ITfThreadMgr:: getglobaldepot**](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-getglobalcompartment)auf.

Der Thread-Manager enthält einen Depot-Manager, der Depots pro Thread enthält. Dadurch können Daten in einem Thread freigegeben werden. Um einen Thread-Manager-Depot-Manager zu erhalten, rufen Sie **ITfThreadMgr:: QueryInterface** mit IID \_ itfgliementmgr auf.

Jeder erstellte Dokument-Manager enthält auch einen Depot-Manager. Dadurch können Daten in einem bestimmten Dokument-Manager freigegeben werden. Um den Depot-Manager für den Dokument-Manager zu erhalten, rufen Sie **ITfDocumentMgr:: QueryInterface** mit IID \_ itfgliementmgr auf.

Jeder erstellte Kontext enthält auch einen Depot-Manager. Dadurch können Daten in einem bestimmten kontextfrei gegeben werden. Rufen Sie zum Abrufen eines Kontext Depot-Managers **ITfContext:: QueryInterface** mit IID \_ itfgliementmgr auf.

## <a name="creating-and-deleting-a-compartment"></a>Erstellen und Löschen eines Depots

Ein Depot wird erstellt, wenn [**itfgliementmgr:: getdepot**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmentmgr-getcompartment) mit der Depot-GUID aufgerufen wird. Der Installations Client sollte den Anfangswert des Depots mithilfe von [**itsdepot:: SetValue**](/windows/desktop/api/Msctf/nf-msctf-itfcompartment-setvalue)festlegen. Der Depot Wert ist leer, bis ein Wert festgelegt ist. Daher gibt es keine Möglichkeit, zu überprüfen, ob das Depot vorhanden war, bevor **getdepot** aufgerufen wurde. Um diese Situation zu vermeiden, sollte der Installations Client den Wert auf einen Anfangswert festlegen, damit andere Clients ermitteln können, ob das Depot bereits vorhanden ist.

Die [**itfgliementmgr:: cleardepot**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmentmgr-clearcompartment) -Methode wird zum Entfernen eines Depots verwendet. Alle vorhandenen Verweise auf das Depot werden als ungültig markiert.

## <a name="obtaining-compartments"></a>Abrufen von Depots

Mithilfe der [**itfgliementmgr**](/windows/desktop/api/Msctf/nn-msctf-itfcompartmentmgr) -Schnittstelle kann ein Client Depots durch Aufrufen von [**itfgliementmgr:: enumdepots**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmentmgr-enumcompartments)aufzählen. Diese Methode stellt ein **ienumguid** -Objekt bereit, das die GUIDs aller installierten Depots enthält.

Mithilfe der Depot-GUID wird **itfgliementmgr:: getdepot** zum Abrufen eines bestimmten Depots verwendet. Diese Methode stellt dem Aufrufer ein [**itfdepot**](/windows/desktop/api/Msctf/nn-msctf-itfcompartment) -Objekt zur Verfügung, das die Depotdaten abrufen und festlegen kann.

## <a name="receiving-compartment-change-notifications"></a>Empfangen von Depot Änderungs Benachrichtigungen

Wenn sich der Wert eines Depots ändert, benachrichtigt der TSF-Manager alle installierten Empfehlung-senken, die das Depot geändert hat. Erstellen Sie ein Objekt, das [**itfmenmenteventsink**](/windows/desktop/api/Msctf/nn-msctf-itfcompartmenteventsink)implementiert, um eine Depot-Änderungs-Senke zu installieren. Rufen Sie dann **itfdepot:: QueryInterface** mit IID \_ itfsource für das Depot-Objekt auf, das überwacht werden soll, um eine [**itfsource**](/windows/desktop/api/Msctf/nn-msctf-itfsource) -Schnittstelle zu erhalten. Nennen Sie nun [**itfsource:: AdviseSink**](/windows/desktop/api/Msctf/nf-msctf-itfsource-advisesink) mit IID \_ itfmenmenteventsink und den Zeiger auf das **itfzersplimenteventsink** -Objekt. Wenn sich der Wert des Depots ändert, wird die [**itfmenmenteventsink:: OnChange**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmenteventsink-onchange) -Eigenschaft der Benachrichtigungs Senke mit der GUID des Depots aufgerufen. Die Hinweis Senke kann [**itfdepot:: GetValue**](/windows/desktop/api/Msctf/nf-msctf-itfcompartment-getvalue) aufrufen, um den neuen Wert zu erhalten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**ITF-mentmgr**](/windows/desktop/api/Msctf/nn-msctf-itfcompartmentmgr)
</dt> <dt>

[**Itmadepot**](/windows/desktop/api/Msctf/nn-msctf-itfcompartment)
</dt> <dt>

[**ITF-menteventsink**](/windows/desktop/api/Msctf/nn-msctf-itfcompartmenteventsink)
</dt> <dt>

[**Tfclientid**](tfclientid.md)
</dt> <dt>

[**ITfThreadMgr:: getglobaldepot**](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-getglobalcompartment)
</dt> <dt>

[**ITF-mentmgr:: getdepot**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmentmgr-getcompartment)
</dt> <dt>

[**ITF Depot:: SetValue**](/windows/desktop/api/Msctf/nf-msctf-itfcompartment-setvalue)
</dt> <dt>

[**ITF-mentmgr:: cleardepot**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmentmgr-clearcompartment)
</dt> <dt>

[**ITF-mentmgr:: enumdepots**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmentmgr-enumcompartments)
</dt> <dt>

[**ITF-Quelle**](/windows/desktop/api/Msctf/nn-msctf-itfsource)
</dt> <dt>

[**ITF Source:: AdviseSink**](/windows/desktop/api/Msctf/nf-msctf-itfsource-advisesink)
</dt> <dt>

[**ITF-menteventsink:: OnChange**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmenteventsink-onchange)
</dt> </dl>

 

 




