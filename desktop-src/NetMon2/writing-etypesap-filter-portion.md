---
description: Der ETYPE/SAP-Teil des Erfassungs Filters benachrichtigt den Netzwerkmonitor Treiber, Frames zu akzeptieren, die über eine bestimmte Kombination von ETYPEs und Dienst Zugriffs Punkten (SAPS) verfügen.
ms.assetid: 57dcf1cd-f27f-4bd3-a5a8-9e978a2d213e
title: Der ETYPE/SAP-Filter Teil wird geschrieben.
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b072d123ca18d3aa2b3f2c91db4a8461473a854
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960341"
---
# <a name="writing-etypesap-filter-portion"></a>Der ETYPE/SAP-Filter Teil wird geschrieben.

Der ETYPE/SAP-Teil des Erfassungs Filters benachrichtigt den Netzwerkmonitor Treiber, Frames zu akzeptieren, die über eine bestimmte Kombination von ETYPEs und [*Dienst Zugriffs Punkten*](s.md) (SAPS) verfügen. ETYPEs und SAPS sind beide Möglichkeiten, wie Protokolle auf niedriger Ebene, z. b. Ethernet, LLC und Snap, welches Protokoll befolgt werden. Dies gilt insbesondere in folgenden Fällen:

-   Ethernet gibt einen ETYPE an
-   LLC gibt einen SAP an
-   "Snap" gibt einen ETYPE an

## <a name="etypesap-capture-filter-flags"></a>ETYPE-/SAP-Erfassungs Filter-Flags

Verwenden Sie die folgenden Informationen, um die Flags im **Filterflags** -Member der [**capturefilter**](capturefilter.md) -Struktur festzulegen.



| Flag                                         | Bedeutung                                                                                                                                                                                                                                                     |
|----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| capturefilter- \_ Flags \_ enthalten \_ alle \_ SAPS   | Übergibt alle SAP-Werte und benachrichtigt den Treiber, dass alle SAP-Werte gültig sind. In Kombination mit Werten im **lpsaptable** -Element benachrichtigt das Flag den Treiber, dass alle SAP-Werte außer den in der **lpsaptable** gültigen sind.<br/>           |
| capturefilter- \_ Flags \_ enthalten \_ alle \_ ETYPEs | Übergibt alle ETYPE-Werte und benachrichtigt den Treiber, dass alle ETYPE-Werte gültig sind. Wenn Sie mit Werten im **lpeer typetable** -Member kombiniert werden, benachrichtigt dieses Flag den Treiber, dass alle ETYPE-Werte außer den Werten in der **lpeer typetable** gültig sind.<br/> |
| capturefilter \_ - \_ Flags \_ nur lokal           | Wenn Sie dieses Flag festlegen, wird eine NIC nicht auf den P-Modus festgelegt. Es wird nur lokaler Datenverkehr (alle Frames zum lokalen Computer) angezeigt.                                                                                                                                          |
| capturefilter- \_ Flags \_ bleiben \_ RAW             | Speichert SMT-und TokenRing-Mac-Frames.                                                                                                                                                                                                                        |



 

## <a name="etypesap-capture-filter-settings"></a>ETYPE/SAP-Erfassungs Filter Einstellungen

Verwenden Sie die folgenden Informationen, um die **lpsaptable** -und **lpetypetable** -Elemente der [**capturefilter**](capturefilter.md) -Struktur festzulegen.



| Einstellung          | Bedeutung                                                                                                                                                                                                                                                              |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **lpsaptable**   | Listet die SAP-Werte auf, die der Treiber übergeben soll. Diese Liste weist den Netzwerkmonitor Treiber an, einen Frame zu validieren, der eine Entsprechung enthält. Wenn die capturefilter- \_ Flags \_ \_ alle \_ SAPS enthalten, wird dies zu einer Ausnahmeliste (sofern gefunden, nicht bestanden).           |
| **lpeer typetable** | Listet die ETYPE-Werte auf, die der Netzwerkmonitor Treiber übergeben soll. Diese Liste allein weist den Treiber an, einen Frame zu validieren, der eine Entsprechung enthält. Wenn die capturefilter- \_ Flags \_ \_ alle \_ ETYPEs festgelegt sind, wird dies zu einer Ausnahmeliste (sofern gefunden, nicht bestanden). |



 

 

 




