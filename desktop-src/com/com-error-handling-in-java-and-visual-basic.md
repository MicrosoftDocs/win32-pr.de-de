---
title: COM-Fehlerbehandlung in Java und Visual Basic
description: COM-Fehlerbehandlung in Java und Visual Basic
ms.assetid: 1130a038-3c18-4530-a6d7-9f538352297f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea12dc040218e14098ce2394fbb5cd2ebeff1704
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104391066"
---
# <a name="com-error-handling-in-java-and-visual-basic"></a>COM-Fehlerbehandlung in Java und Visual Basic

Es gibt drei Schnittstellen und drei Funktionen, die in com verwendet werden können, um Fehlerbehandlung bei der Programmierung in Java oder Microsoft Visual Basic bereitzustellen. In Java und Visual Basic gibt der Methoden Aufrufwert kein **HRESULT** als Rückgabewert zurück. Stattdessen verwenden diese Sprachen die COM-Schnittstellen und-Funktionen zum Abrufen von **HRESULT** -Werten und zum Behandeln von Fehlern oder Ausnahmen. (Ausnahmen sind Ereignisse, die über das Programm gesteuert werden, wie z. b. Datei Probleme oder ungültige Parameter.)

Die drei Schnittstellen, die **HRESULT** s unterstützen, werden in der folgenden Tabelle aufgeführt und kurz beschrieben.



|                                                                          |                                                                                                                      |
|--------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [**Ikreateerrorinfo**](/windows/win32/api/oaidl/nn-oaidl-icreateerrorinfo)<br/>  | Legt Fehlerinformationen fest.<br/>                                                                                   |
| [**IErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo)<br/>        | Gibt Informationen von einem Fehler Objekt zurück.<br/>                                                                 |
| [**ISupportErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-isupporterrorinfo)<br/> | Identifiziert das-Objekt als Unterstützung der [**IErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo) -Schnittstelle.<br/> |



 

Die drei Funktionen, die **HRESULT** s unterstützen, werden in der folgenden Tabelle aufgeführt und kurz beschrieben.



|                                                                        |                                                                                                                                                                      |
|------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**"Kreateerrorinfo"**](/windows/win32/api/oleauto/nf-oleauto-createerrorinfo)<br/> | Erstellt eine Instanz eines generischen Fehler Objekts.<br/>                                                                                                            |
| [**GetErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-geterrorinfo)<br/>    | Ruft den Fehler Informations Zeiger ab, der durch den vorherigen Aufrufs von [**SetErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-seterrorinfo) im aktuellen logischen Thread festgelegt wurde.<br/> |
| [**SetErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-seterrorinfo)<br/>    | Legt das Fehler Informationsobjekt für den aktuellen Ausführungs Thread fest.<br/>                                                                                    |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Fehlerbehandlung in com](error-handling-in-com.md)
</dt> </dl>

 

