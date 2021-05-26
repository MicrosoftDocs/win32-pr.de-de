---
title: COM-Fehlerbehandlung in Java und Visual Basic
description: COM-Fehlerbehandlung in Java und Visual Basic
ms.assetid: 1130a038-3c18-4530-a6d7-9f538352297f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11c55c1c2414c69ff9398845858baadebd58cbf9
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2021
ms.locfileid: "110424010"
---
# <a name="com-error-handling-in-java-and-visual-basic"></a>COM-Fehlerbehandlung in Java und Visual Basic

Es gibt drei Schnittstellen und drei Funktionen, die in COM verwendet werden können, um fehlerbehandlung bei der Programmierung in Java oder Microsoft Visual Basic. In Java und Visual Basic gibt der Methodenaufruf kein **HRESULT** als Rückgabewert zurück. Stattdessen verwenden diese Sprachen die COM-Schnittstellen und -Funktionen, um **HRESULT-Werte** zu erhalten und Fehler oder Ausnahmen zu behandeln. (Ausnahmen sind Ereignisse, die außerhalb der Kontrolle des Programms liegen, z. B. Dateiprobleme oder ungültige Parameter.)

Die drei Schnittstellen, die **HRESULT-Unterstützung** bieten, sind in der folgenden Tabelle kurz aufgeführt und beschrieben.



|  Schnittstelle                                                                        |  BESCHREIBUNG                                                                                                                    |
|--------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [**ICreateErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-icreateerrorinfo)<br/>  | Legt Fehlerinformationen fest.<br/>                                                                                   |
| [**IErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo)<br/>        | Gibt Informationen aus einem Fehlerobjekt zurück.<br/>                                                                 |
| [**ISupportErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-isupporterrorinfo)<br/> | Identifiziert das -Objekt als unterstützung für die [**IErrorInfo-Schnittstelle.**](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo)<br/> |



 

Die drei Funktionen, die **HRESULT-Unterstützung** bieten, sind in der folgenden Tabelle kurz aufgeführt und beschrieben.



|    Schnittstelle       |       BESCHREIBUNG       |
|------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-createerrorinfo)<br/> | Erstellt eine Instanz eines generischen Fehlerobjekts.<br/>                                                                                                            |
| [**GetErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-geterrorinfo)<br/>    | Erhält den Fehlerinformationszeiger, der durch den vorherigen Aufruf von [**SetErrorInfo im**](/windows/win32/api/oleauto/nf-oleauto-seterrorinfo) aktuellen logischen Thread festgelegt wurde.<br/> |
| [**SetErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-seterrorinfo)<br/>    | Legt das Fehlerinformationsobjekt für den aktuellen Ausführungsthread fest.<br/>                                                                                    |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Fehlerbehandlung in COM](error-handling-in-com.md)
</dt> </dl>

 

