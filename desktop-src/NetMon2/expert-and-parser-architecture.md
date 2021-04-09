---
description: Die folgende Abbildung zeigt die Beziehung zwischen Experten-und parseranwendungen und anderen Komponenten der Netzwerkmonitor Architektur.
ms.assetid: f943f0e6-5fdc-48f9-ba5d-5effdf8229f3
title: Architektur von Experten und Parsers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: caa8477d97604acfb04686170ca6cb5cff8116a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128361"
---
# <a name="expert-and-parser-architecture"></a>Architektur von Experten und Parsers

Die folgende Abbildung zeigt die Beziehung zwischen [Experten](experts.md) -und [parseranwendungen](parsers.md) und anderen Komponenten der Netzwerkmonitor Architektur.

![die Beziehung zwischen Experten-und parseranwendungen](images/nm-arch1.png)

Der Netzwerk Datenverkehr wird als einzelne Frames vom NDIS-Treiber gesammelt. Der Netzwerkmonitor Treiber (Nmnt.sys) leitet die Frames dann an einen Netzwerk Paketanbieter (NPP) weiter, der die Daten erfasst und in einer oder mehreren Erfassungs Dateien platziert. Der npp ist eine Sammlung von COM-Schnittstellen, die zum Erfassen von Daten verwendet werden. In diesem Fall wird die [**idelta-DC**](idelaydc.md) -Schnittstelle verwendet, um eine verzögerte Erfassung auszuführen.

> [!Note]  
> Der NPP wird für verzögerte und Echt Zeit Erfassungen verwendet. Für echt Zeit Erfassungen [**wird die-**](irtc.md) Schnittstelle verwendet.

 

Wenn die Netzwerk Frames in der Erfassungs Datei gespeichert werden und auf die Datei zugegriffen werden kann, können Experten und Parser die Netzwerkmonitor-Benutzeroberfläche und die Netzwerkmonitor Funktionen verwenden, die in Nmapi.dll zur Analyse der Daten bereitgestellt werden. Auf Erfassungs Dateien kann erst dann zugegriffen werden, wenn die Erfassung beendet ist.

 

 



