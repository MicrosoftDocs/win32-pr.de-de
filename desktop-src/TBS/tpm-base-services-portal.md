---
title: TPM-Basisdienste
description: Die TPM-Software stellt Dienste als API bereit, die durch Remote Prozedur Aufrufe verfügbar gemacht wird. Verwenden Sie TPM, um ein TPM-Modul zu erstellen.
ms.assetid: ae6e7fe9-585d-467a-8456-e008b8ea89a0
keywords:
- TDie Basisdienste-TSB von TPM
- Basisdienste für TPM, Startseite
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d2cbdfc1f85d6917f2e9a7a5b8e7a0fc25ebdc8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390682"
---
# <a name="tpm-base-services"></a>TPM-Basisdienste

## <a name="purpose"></a>Zweck

Die TPM-Funktion (Trusted Platform Module) zentralisiert den TPM-Zugriff auf Anwendungen.

Das TSB-Feature wird als Systemdienst in Windows Server 2008, Windows Vista oder neueren Betriebssystemen ausgeführt. Dienste werden als API bereitgestellt, die über Remote Prozedur Aufrufe (RPC) verfügbar gemacht wird. Das TSB-Feature verwendet Prioritäten, die durch den Aufruf von Anwendungen festgelegt werden, um den TPM-Zugriff zusammen

> [!Note]
>
> Das TPM kann für Schlüsselspeicher Vorgänge verwendet werden. Entwicklern wird jedoch empfohlen, stattdessen die [Schlüsselspeicher-APIs](/windows/desktop/SecCNG/key-storage-and-retrieval) für diese Szenarien zu verwenden. Die Schlüsselspeicher-APIs bieten die Funktionalität zum Erstellen, signieren oder verschlüsseln mit Kryptografieschlüsseln und sind auf höherer Ebene und leichter zu verwenden als die TSB für diese Ziel Szenarien.

 

## <a name="developer-audience"></a>Entwicklergruppe

TSB ist für die Verwendung durch Entwickler von Anwendungen basierend auf den Windows-Betriebssystemen vorgesehen. Entwickler sollten mit den Programmiersprachen C und C++ und der Microsoft Windows-Programmierumgebung vertraut sein.

## <a name="run-time-requirements"></a>Laufzeitanforderungen

Das TSB-Feature erfordert mindestens das Betriebssystem Windows Server 2008 oder Windows Vista. Informationen zu den Lauf Zeitanforderungen für ein bestimmtes Programmier Element finden Sie im Abschnitt "Anforderungen" der Referenzseite für dieses Element.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                         | BESCHREIBUNG                                                                     |
|-----------------------------------------------|---------------------------------------------------------------------------------|
| [Informationen zu TSB](about-tbs.md)<br/>         | Wichtige Konzepte und eine allgemeine Übersicht über das TSB-Feature.<br/>               |
| [Verwenden von TSB](using-tbs.md)<br/>         | TSB-Prozesse und-Prozeduren für die Verwendung der TSB-API.<br/>                  |
| [TSB-Referenz](tbs-reference.md)<br/> | Dokumentation zu den TSB-Funktionen,-Strukturen und-Rückgabecodes.<br/> |



 

 

