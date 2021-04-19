---
description: Wenn Sie benutzerdefinierte Erweiterungen erstellen oder eine komplexe Erweiterung codieren möchten, können Sie eigene Erweiterungs Handler schreiben, mit denen benutzerdefinierte Schnittstellen exportiert werden.
ms.assetid: a33ac417-b5f9-4ad7-a26e-13cdb1e4ac1b
title: Schreiben von benutzerdefinierten Erweiterungs Handlern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61c8c4380b11fd0b0b1a5484ba0a7ab80f69c967
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364160"
---
# <a name="writing-custom-extension-handlers"></a>Schreiben von benutzerdefinierten Erweiterungs Handlern

Wenn Sie benutzerdefinierte Erweiterungen erstellen oder eine komplexe Erweiterung codieren möchten, können Sie eigene Erweiterungs Handler schreiben, mit denen benutzerdefinierte Schnittstellen exportiert werden. Die Microsoft-Zertifikat Dienste werden mit den folgenden Schnittstellen ausgeliefert, die zum Codieren verschiedener Erweiterungs Datentypen verwendet werden können: [**icertencodealtname**](/windows/desktop/api/Certenc/nn-certenc-icertencodealtname), [**icertencodebitstring**](/windows/desktop/api/Certenc/nn-certenc-icertencodebitstring), [**icertencodecrldistinfo**](/windows/desktop/api/Certenc/nn-certenc-icertencodecrldistinfo), [**icertencodedatearray**](/windows/desktop/api/Certenc/nn-certenc-icertencodedatearray), [**icertencodelta ongarray**](/windows/desktop/api/Certenc/nn-certenc-icertencodelongarray)und [**icertencodestringarray**](/windows/desktop/api/Certenc/nn-certenc-icertencodestringarray). Diese Schnittstellen sind in Certenc.dll enthalten. Außerdem sind die Typinformationen für diese Schnittstellen in Certencl.dll enthalten, das im Platform Software Development Kit (SDK) enthalten ist.

Weitere Informationen zu Erweiterungs Handlern finden Sie unter [Erweiterungs Handler](extension-handlers.md).

 

 



