---
title: Sicherheitsüberlegungen für Windows Color System
description: Sicherheitsüberlegungen für Windows Color System
ms.assetid: 9e8b7c38-3c4f-4537-a7e1-6ad0daa39497
keywords:
- Windows Farbsystem (WCS), Sicherheit
- WCS (Windows Color System), Sicherheit
- Bildfarbverwaltung, Sicherheit
- Farbverwaltung, Sicherheit
- Sicherheit für Windows Color System (WCS)
- Color Management Module (CMM)
- CMM (Farbverwaltungsmodul)
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e710a0224c10d4f7cd7aa1565e88d00da539370974719129a37d735f11a29fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118444667"
---
# <a name="security-considerations-windows-color-system"></a>Sicherheitsüberlegungen: Windows Color System

Dieses Dokument enthält Informationen zu Sicherheitsüberlegungen im Zusammenhang mit der Bildfarbverwaltung. Dieses Dokument enthält nicht alles, was Sie über Sicherheitsprobleme wissen müssen. Verwenden Sie es stattdessen als Ausgangspunkt und Referenz für diesen Technologiebereich.

## <a name="non-microsoft-cmms-can-run-in-system-context"></a>Nicht-Microsoft-CMMs können im Systemkontext ausgeführt werden.

Nicht-Microsoft-Farbverwaltungsmodule (CmMs) sollten wie Nicht-Microsoft-Druckertreiber behandelt werden, da sie in einem Systemkontext für Druckvorgänge ausgeführt werden können.
