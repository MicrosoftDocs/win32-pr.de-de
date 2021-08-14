---
description: Die folgende Abbildung zeigt die Beziehung zwischen Experten- und Parseranwendungen und anderen Komponenten der Netzwerkmonitor Architektur.
ms.assetid: f943f0e6-5fdc-48f9-ba5d-5effdf8229f3
title: Experten- und Parserarchitektur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 261343005f0cb9fc7de5b7025f9ffe59f11515614ab43609c1b8da9f396e9f5e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117795841"
---
# <a name="expert-and-parser-architecture"></a>Experten- und Parserarchitektur

Die folgende Abbildung zeigt die Beziehung zwischen [Experten-](experts.md) und [Parseranwendungen](parsers.md) und anderen Komponenten der Netzwerkmonitor Architektur.

![Beziehung zwischen Experten- und Parseranwendungen](images/nm-arch1.png)

Der Netzwerkdatenverkehr wird als einzelne Frames vom NDIS-Treiber erfasst. Der Netzwerkmonitor-Treiber (Nmnt.sys) leitet die Frames dann an einen Netzwerkpaketanbieter (Network Packet Provider, NPP) weiter, der die Daten erfasst und in mindestens einer Erfassungsdateien platziert. Der NPP ist eine Sammlung von COM-Schnittstellen, die zum Erfassen von Daten verwendet werden. In diesem Fall wird die [**IDelaydC-Schnittstelle**](idelaydc.md) verwendet, um eine verzögerte Erfassung durchzuführen.

> [!Note]  
> Der NPP wird für verzögerte und Echtzeiterfassungen verwendet. Für Echtzeiterfassungen wird die [**IRTC-Schnittstelle**](irtc.md) verwendet.

 

Wenn die Netzwerkframes in der Erfassungsdatei gespeichert sind und auf die Datei zugegriffen werden kann, können Experten und Parser die Netzwerkmonitor-Benutzeroberfläche und die Netzwerkmonitor-Funktionen verwenden, die in Nmapi.dll bereitgestellt werden, um die Daten zu analysieren. Auf Erfassungsdateien kann erst zugegriffen werden, wenn die Erfassung abgeschlossen ist.

 

 



