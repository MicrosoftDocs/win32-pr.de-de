---
description: Übersicht über die Architektur
ms.assetid: ff20d83a-e9cd-46e9-95f7-3ebdf791e667
title: Übersicht über die Architektur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76eafce326655a4d9386d37c02df9ef0ab2b9772b5e87eedaff40a19383b2cec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119590465"
---
# <a name="architecture-overview"></a>Übersicht über die Architektur

Die WPD-Architektur kann in drei Prozesse unterteilt werden. Innerhalb dieser Prozesse befinden sich die drei Hauptkomponenten von WPD: die API, das Serialisierungs- und der Treiber. Die folgende Abbildung zeigt die Prozesse und Komponenten, die die WPD-Architektur bilden.

![Abbildung der API-, Serialisierungs- und Treiberkomponenten von wpd](images/wpd-overview-figure1.gif)

## <a name="the-wpd-application-programming-interface"></a>Die WPD-Anwendungsprogrammierschnittstelle

Die WPD-API wird als in-proc-COM-Server implementiert. Die API verwendet Microsoft Win32-Standard-APIs für die Kommunikation mit dem entsprechenden WPD-Treiber. Eine Komponente namens WPD-Serialisierung wird sowohl von API-Objekten als auch vom Treiber zum Packen oder Entpacken von Parametern in oder aus umDF-Puffern (Windows Driver Foundation)-User-Mode Driver Framework (UMDF) verwendet.

## <a name="the-wpd-serializer"></a>Das WPD-Serialisierungs-

Das WPD-Serialisierungs-Unternehmen wird als in-proc-COM-Server implementiert. Die WPD-API verwendet das Serialisierungspaket, um Befehle und Parameter in Nachrichtenpuffer zu packen, die an den Treiber gesendet werden. Der Treiber verwendet das Serialisierungspaket, um diese Nachrichtenpuffer für die Verarbeitung zu entpacken. Der Treiber verwendet auch das Serialisierungspaket, um Daten und Parameter in Antwortpuffer zu packen, die an die WPD-API zurückgegeben werden, und die WPD-API verwendet das Serialisierungspaket, um diese Antwortpuffer zu entpacken, um an Aufrufer zurückzukehren.

## <a name="wpd-driver"></a>WPD-Treiber

Der WPD-Treiber wird alsF-Treiber (Windows Driver Foundation)-User-Mode Driver Framework (UMDF) implementiert. WPD-Treiber werden von UMDF in einem separaten Prozess gehostet, der als Treiberhost bezeichnet wird.

Der Treiber empfängt Nachrichten vom UMDF-Reflektor (dies ist im Diagramm nicht dargestellt, da es für den Treiber nicht wichtig ist, wie die Puffer empfangen werden). Weitere Informationen finden Sie in der UMDF-Dokumentation. Der Treiber implementiert einen WPD-spezifischen IOCL-Handler (I/O Control Code), um von der WPD-API empfangene WPD-Nachrichten zu verarbeiten. Der Treiber verwendet das WPD-Serialisierungspaket, um Befehle und Parameter aus diesen Nachrichtenpuffern zu entpacken und die Antwort in den Rückgabepuffer zu packen.

WPD-Treiber können mit ihren Geräten kommunizieren, indem sie einen Kernelmodustreiber verwenden, auf den in der Regel über Win32-Dateivorgänge zugegriffen wird (d. h. CreateFile, ReadFile, WriteFile und so weiter). Für die gängigen Buslinien stellt Microsoft Standardkerneltreiber für Hersteller zur Verfügung, die es Anbietern ermöglichen, eine Treiberlösung nur im Benutzermodus zu liefern. Darüber hinaus stellt Microsoft für MTP-Geräte (Media Transfer Protocol) und MSC-Geräte (Mass Storage Class) WPD-Klassentreiber zur Verfügung.

Weitere Informationen zu WPD-Treibern finden Sie in der dokumentation Windows Portable Devices Driver im Windows Driver Kit.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Anwendungsübersicht**](application-overview.md)
</dt> </dl>

 

 



