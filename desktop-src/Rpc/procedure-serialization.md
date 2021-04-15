---
title: Prozessserialisierung
description: Wenn Sie die Prozedur-Serialisierung verwenden, wird eine Prozedur mit dem Attribut \ codieren \ oder \ Decode \ bezeichnet. Anstatt den üblichen RemoteStub zu generieren, generiert der Compiler einen serialisierungsstub für die Routine.
ms.assetid: 98367b00-696b-44c4-a747-92ecac34ba1e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77696761a9aa5fe1471e9ebf24a57303b15d0ff3
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "104393877"
---
# <a name="procedure-serialization"></a>Prozessserialisierung

Wenn Sie die Prozedur-Serialisierung verwenden, wird eine Prozedur mit dem \[ Attribut [**Codieren**](/windows/desktop/Midl/encode) \] oder \[ [**decodieren**](/windows/desktop/Midl/decode) bezeichnet \] . Anstatt den üblichen RemoteStub zu generieren, generiert der Compiler einen serialisierungsstub für die Routine.

Ebenso wie eine Remote Prozedur ein Bindungs Handle für einen Remote-Befehl verwenden muss, muss bei einer Serialisierungsprozedur ein serialisierungshandle verwendet werden, um Serialisierungsdienste zu verwenden. Wenn kein serialisierungshandle angegeben ist, wird ein implizites implizites Handle zum Weiterleiten des Aufrufes verwendet. Wenn das serialisierungshandle hingegen entweder als explizites [**handle \_ t**](/windows/desktop/Midl/handle-t) -Argument der Routine oder mithilfe des \[ [**expliziten \_ handle**](/windows/desktop/Midl/explicit-handle) - \] Attributs angegeben wird, müssen Sie ein gültiges Handle als Argument des Aufrufes übergeben. Weitere Informationen zum Erstellen eines gültigen serialisierungshandles finden Sie unter [serialisierungshandles](serialization-handles.md), [Beispiele für die festgelegte Puffer Codierung](fixed-buffer-serialization.md)und [Beispiele für die inkrementelle Codierung](examples-of-incremental-encoding.md).

> [!Note]
> Mit Microsoft RPC können Remote-und serialisierungsprozeduren in einer einzigen Schnittstelle gemischt werden. Verwenden Sie hierfür jedoch Vorsicht.
> 
> Für Remote Prozeduren mit impliziten Bindungs Handles generiert der-compilercompiler eine globale handle-Variable vom Typ [**handle \_ t**](/windows/desktop/Midl/handle-t). Prozeduren und Typen mit impliziten serialisierungshandles verwenden dieselbe globale handle-Variable.
> 
> Bei impliziten Handles muss das globale implizite handle vor einem Remote-Befehl auf ein gültiges Bindungs handle festgelegt werden. Das implizite Handle muss vor einem serialisierungsbefehl auf ein gültiges serialisierungshandle festgelegt werden. Daher kann eine Prozedur nicht sowohl Remote als auch serialisiert werden. Der Wert muss ein oder der andere sein.

 

 

 