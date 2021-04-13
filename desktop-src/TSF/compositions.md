---
title: Ablage
description: Eine Komposition ist ein temporärer Eingabe Zustand, der es einem Text Dienst ermöglicht, sowohl für die Anwendung als auch für den Benutzer anzugeben, dass sich der Eingabetext noch im Zustand der Änderung befindet.
ms.assetid: 3d9da4f2-ceb9-4abc-8979-d3756d948a57
keywords:
- Text Dienst Framework (TSF), Kompositionen
- TSF (Text Dienst Framework), Kompositionen
- Text Dienste, Kompositionen
- TSF-aktivierte Anwendungen, Kompositionen
- compositions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b03f3e991f76ee7c6dca3830267796576c7b842
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390791"
---
# <a name="compositions"></a>Ablage

Eine Komposition ist ein temporärer Eingabe Zustand, der es einem Text Dienst ermöglicht, sowohl für die Anwendung als auch für den Benutzer anzugeben, dass sich der Eingabetext noch im Zustand der Änderung befindet. Eine Anwendung kann Anzeige Attributinformationen über die Komposition abrufen und diese Informationen verwenden, um dem Benutzer den Kompositions Status anzuzeigen.

Ein Beispiel für die Verwendung einer Komposition ist die Spracheingabe. Während der Benutzer spricht, erstellt der sprach Text Dienst eine Komposition. Diese Komposition bleibt intakt, bis die gesamte Spracheingabe vollständig ist. Wenn die Sitzung beendet wird, beendet der sprach Text Dienst die Komposition.

Eine Anwendung verwendet das vorhanden sein und Nichtvorhandensein einer Komposition, um zu bestimmen, wie Text angezeigt wird und was, falls vorhanden, die Verarbeitung für den Text ausgeführt werden soll. Wenn der Benutzer z. b. die Sprach-Engine zum Eingeben von Text verwendet, sollte die Anwendung keine Rechtschreibprüfung oder Grammatik Überprüfung für einen Kompositions Text durchführen. Der Text wird bis zur Beendigung der Komposition als unvollständig betrachtet.

## <a name="text-services"></a>Text Dienste

Ein Text Dienst erstellt eine Komposition durch Aufrufen von [itfcontextcomposition:: StartComposition](/windows/desktop/api/msctf/nf-msctf-itfcontextcomposition-startcomposition). Der Text Dienst kann optional ein [ITF compositionsink](/windows/desktop/api/msctf/nn-msctf-itfcompositionsink) -Objekt implementieren, das Kompositions Ereignis Benachrichtigungen empfängt. StartComposition gibt ein [itfcomposition](/windows/desktop/api/msctf/nn-msctf-itfcomposition) -Objekt zurück, auf das der Text Dienst einen Verweis speichert und das verwendet, um die Komposition zu ändern und zu beenden. Der Text Dienst beendet die Komposition durch Aufrufen von [itfcomposition:: endcomposition](/windows/desktop/api/msctf/nf-msctf-itfcomposition-endcomposition).

Wenn ein Text Dienst Kompositionen erstellen soll, sollte er auch Anzeige Attribute unterstützen, damit eine Anwendung Text, der Teil einer Komposition ist, anders als Standardtext anzeigen kann. Weitere Informationen finden Sie unter [Bereitstellen von Anzeige Attributen](providing-display-attributes.md).

## <a name="applications"></a>Anwendungen

Eine Anwendung kann die Erstellung, Änderung und Beendigung von Kompositionen überwachen, indem eine [itfcontextownercompositionsink](/windows/desktop/api/msctf/nn-msctf-itfcontextownercompositionsink) -Senke installiert wird. Wenn eine Komposition gestartet wird, wird [itfcontextownercompositionsink:: onstartcomposition](/windows/desktop/api/msctf/nf-msctf-itfcontextownercompositionsink-onstartcomposition) aufgerufen. Ebenso werden, wenn eine Komposition geändert oder beendet wird, [itfcontextownercompositionsink:: onupdatecomposition](/windows/desktop/api/msctf/nf-msctf-itfcontextownercompositionsink-onupdatecomposition) und [itfcontextownercompositionsink:: onendcomposition](/windows/desktop/api/msctf/nf-msctf-itfcontextownercompositionsink-onendcomposition) aufgerufen.

Im folgenden finden Sie ein typisches Verfahren zum Aktualisieren eines Dokuments mithilfe einer Komposition.

1.  [ITextStoreACP:: inserttextatselection](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-inserttextatselection) oder [itextstoreanchor:: inserttextatselection](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-inserttextatselection) wird normalerweise verwendet, um den anfänglichen Text in die Komposition einzufügen.
2.  Die Komposition wird mit einem Aufrufen von [itfcontextcomposition:: StartComposition](/windows/desktop/api/Msctf/nf-msctf-itfcontextcomposition-startcomposition)gestartet, wobei der von **inserttextatselection** zurückgegebene Textbereich verwendet wird.
3.  Wenn Sie neue Eingaben wie Sprache oder Tastatureingabe empfängt, aktualisiert die Anwendung die Komposition mit [ITextStoreACP:: SetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-settext) oder [itextstoreanchor:: SetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-settext).
4.  Wenn die Anwendung feststellt, dass es an der Zeit ist, die Komposition zu beenden, wird [itfcomposition:: endcomposition](/windows/desktop/api/Msctf/nf-msctf-itfcomposition-endcomposition)aufgerufen.

Die Anwendung sollte die Anzeige Attribute verwenden, die vom Text Dienst bereitgestellt werden, um die Anzeige von Text jederzeit zu ändern, und nicht nur, wenn eine Komposition aktiv ist. Weitere Informationen finden Sie unter [Verwenden von Anzeige Attributen](using-display-attributes.md).

Bei Bedarf kann eine Anwendung eine Komposition beenden, indem [itfcontextownercompositionservices:: terminatecomposition](/windows/desktop/api/msctf/nf-msctf-itfcontextownercompositionservices-terminatecomposition)aufgerufen wird.

 

 