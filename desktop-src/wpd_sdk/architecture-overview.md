---
description: Übersicht über die Architektur
ms.assetid: ff20d83a-e9cd-46e9-95f7-3ebdf791e667
title: Übersicht über die Architektur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15f911a14e60465efc8f8f8d798b7ddf527bf4e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868271"
---
# <a name="architecture-overview"></a>Übersicht über die Architektur

Die WPD-Architektur kann in drei Prozesse unterteilt werden. Innerhalb dieser Prozesse sind die drei primären Komponenten von WPD: die API, das Serialisierungsprogramm und der Treiber. In der folgenden Abbildung werden die Prozesse und Komponenten dargestellt, die die WPD-Architektur bilden.

![Abbildung der API-, Serialisierungsprogramme-und Treiber Komponenten von WPD](images/wpd-overview-figure1.gif)

## <a name="the-wpd-application-programming-interface"></a>Die WPD-Anwendungsprogrammierschnittstelle

Die WPD-API wird als in-proc-com-Server implementiert. Die API verwendet standardmäßige Microsoft-Win32-APIs, um mit dem entsprechenden WPD-Treiber zu kommunizieren. Eine Komponente, die als WPD-Serialisierungsprogramm bezeichnet wird, wird sowohl von API-Objekten als auch vom Treiber verwendet, um Parameter in oder aus Windows Driver Foundation (WDF)-, User-Mode Driver Framework

## <a name="the-wpd-serializer"></a>Der WPD-Serialisierer

Das WPD-Serialisierungsprogramm wird als in-proc-com-Server implementiert. Die WPD-API verwendet das Serialisierungsprogramm, um Befehle und Parameter in Nachrichten Puffer zu packen, die an den Treiber gesendet werden. Der Treiber verwendet das Serialisierungsprogramm, um diese Nachrichten Puffer für die Verarbeitung zu entpacken. Der Treiber verwendet auch das Serialisierungsprogramm zum Packen von Daten und Parametern in Antwort Puffer, die an die WPD-API zurückgegeben werden, und die WPD-API verwendet das Serialisierungsprogramm, um diese Antwort Puffer zum zurückkehren zu Aufrufern zu entpacken.

## <a name="wpd-driver"></a>WPD-Treiber

Der WPD-Treiber ist als Standardtreiber für Windows Driver Foundation (WDF), User Mode Driver Framework (UMDF) implementiert. WPD-Treiber werden von der-Funktion in einem separaten Prozess gehostet, der als Treiber Host bezeichnet wird.

Der Treiber empfängt Nachrichten vom Umschlag "um DF" (Dies wird im Diagramm nicht angezeigt, da die Puffer Informationen für den Treiber nicht wichtig sind. Weitere Informationen finden Sie in der Umschlag Dokumentation.) Der Treiber implementiert einen WPD-spezifischen e/a-Steuerungs Code (iocl)-Handler, um von der WPD-API empfangene WPD-Nachrichten zu verarbeiten. Der Treiber verwendet das WPD-Serialisierungsprogramm, um Befehle und Parameter aus diesen Nachrichten Puffern zu entpacken und die Antwort in den Rückgabe Puffer zu packen.

WPD-Treiber können mit ihren Geräten kommunizieren, indem Sie einen Kernelmodustreiber durchlaufen. der Zugriff erfolgt in der Regel über Win32-Datei Vorgänge (d. h. "", "", "", "", "Write file" usw.) Bei den gängigen Bussen werden von Microsoft standardmäßige Kernel Treiber für die zu verwendenden Anbieter bereitgestellt, die es Anbietern ermöglichen, eine Treiber Lösung im Benutzermodus zu liefern. Darüber hinaus stellt Microsoft für MTP-Geräte (Media Transfer Protocol) und MSC-Geräte (Massenspeicher Klasse) WPD-Klassen Treiber bereit.

Weitere Informationen zu WPD-Treibern finden Sie im Windows-Treiberkit unter Treiber Dokumentation für tragbare Windows-Geräte.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Anwendungs Übersicht**](application-overview.md)
</dt> </dl>

 

 



