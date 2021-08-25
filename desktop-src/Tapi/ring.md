---
description: Ein einzelnes Telefon kann möglicherweise mit unterschiedlichen Ringmodi anrufen.
ms.assetid: c5ddcb3c-183c-4f97-9429-977d5cc32668
title: Ring
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5d183c217447ca02bf5ee0c535360eecaea1f3c209cdb813ad58b77268f234d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119773360"
---
# <a name="ring"></a>Ring

Ein einzelnes Telefon kann möglicherweise mit unterschiedlichen Ringmodi anrufen. Angesichts der Vielzahl der verfügbaren Ringmodi werden Ringmodi anhand ihrer Ringmodusnummer identifiziert. Eine Ringmodusnummer reicht von 0 bis zur Anzahl der verfügbaren Ringmodi minus 1.

Die Funktionen, die eine Anwendung verwenden würde, um die Ringmodi eines Telefongeräts zu steuern, sind [**phoneSetRing**](/windows/desktop/api/Tapi/nf-tapi-phonesetring), das ein offenes Telefongerät gemäß einem bestimmten Ringmodus ringt, und [**phoneGetRing**](/windows/desktop/api/Tapi/nf-tapi-phonegetring), das den aktuellen Ringmodus eines geöffneten Telefongeräts zurückgibt.

Wenn der Ringmodus eines Telefongeräts geändert wird, wird eine [**PHONE \_ STATE-Nachricht**](phone-state.md) an die Anwendung gesendet, um die Anwendung über die Zustandsänderung zu benachrichtigen. Parameter für diese Meldung geben einen Hinweis auf die Änderung.

 

 



