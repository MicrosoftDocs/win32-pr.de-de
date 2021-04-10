---
title: Idleon-Eigenschaft
description: Idleon-Eigenschaft
ms.assetid: ba436dec-c7b4-42e8-99d6-c6ff93afd73c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53e7fcec4bd6e163baab7722e4d893146819408a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309139"
---
# <a name="idleon-property"></a>Idleon-Eigenschaft

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Gibt einen booleschen Wert zurück, der bestimmt, ob der Server die **idlinger** -Zustands Animationen des angegebenen Zeichens verwaltet, oder legt diesen fest.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*Agent ***. Zeichen ("*** Merkmal-ID * * *"). Idleon*- *  \[  =  *boolescher* Wert\]

</dd> </dl> 

| Teil      | BESCHREIBUNG                                                                                                                                                                                                             |
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *boolean* | Ein boolescher Ausdruck, der angibt, ob der Server den Leerlauf Modus verwaltet. **True** (Standard) die Server Behandlung des Leerlauf Status ist aktiviert. <br/> **False** Die Server Behandlung des Leerlauf Zustands ist deaktiviert. <br/> |



 

## <a name="remarks"></a>Bemerkungen

Der Server legt automatisch ein Timeout fest, nachdem die letzte Animation für ein Zeichen wiedergegeben wurde. Wenn das Intervall des Zeit Gebers abgelaufen ist, beginnt der Server mit dem **Leerlauf** Zustand für ein Zeichen, wobei die zugehörigen **idck** -Animationen in regelmäßigen Abständen abgespielt werden. Wenn Sie verhindern möchten, dass der Server die **idck** -Zustands Animationen automatisch wieder gibt, legen Sie die-Eigenschaft auf " **false** " fest, und wiedergeben Sie eine Animation oder rufen Sie [**die Methode "**](stop-method.md) Das Festlegen dieses Werts wirkt sich nicht auf den aktuellen Animations Zustand des Zeichens aus.

Diese Eigenschaft gilt nur für die Verwendung des Zeichens durch die Client Anwendung. Diese Einstellung wirkt sich nicht auf andere Clients des Zeichens oder andere Zeichen ihrer Client Anwendung aus.

 

 





