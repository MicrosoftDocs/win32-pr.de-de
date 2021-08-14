---
description: Sie können symmetrische Schlüssel und asymmetrische Schlüssel mit CNG importieren und exportieren. Außerdem können Sie schlüsselexport- und import-Funktionen verwenden, um Schlüssel zwischen Computern zu verschieben.
ms.assetid: 37bda1e0-5dd2-455c-9627-4e7e1b0e04d3
title: Schlüsselimport und -export
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a4b6c26069911d771697bf06f7464aa14ab7f099e4a0e06991d2fd992efa44a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118907701"
---
# <a name="key-import-and-export"></a>Schlüsselimport und -export

Sie können symmetrische Schlüssel [*und asymmetrische Schlüssel mit*](/windows/desktop/SecGloss/s-gly) CNG importieren und exportieren. Außerdem können Sie schlüsselexport- und import-Funktionen verwenden, um Schlüssel zwischen Computern zu verschieben.

## <a name="symmetric-keys"></a>Symmetrische Schlüssel

Um symmetrische Schlüssel (oder Sitzungsschlüssel) zu importieren oder zu exportieren, in denen derselbe Schlüssel zum Verschlüsseln und Entschlüsseln einiger Daten verwendet wird, können Sie die [**Funktionen BCryptImportKey**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptimportkey) und [**BCryptExportKey**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptexportkey) verwenden. In der Regel exportieren Sie zunächst einen Schlüssel mithilfe der **BCryptExportKey-Funktion,** bevor Sie mithilfe der **BCryptImportKey-Funktion** importieren. Die Funktionen sind so konzipiert, dass die Verschlüsselung exportierter und importierter Schlüssel mithilfe der *Parameter hExportKey* und *hImportKey aktiviert* wird. Die Microsoft-Implementierung dieser Funktionen unterstützt jedoch keine Verschlüsselung von exportierten und importierten Schlüsseln.

## <a name="asymmetric-keys"></a>Asymmetrische Schlüssel

Um asymmetrische (oder [*öffentliche/private)*](/windows/desktop/SecGloss/p-gly)Schlüsselpaare zu importieren, in denen ein Schlüssel zum Verschlüsseln und der andere zum Entschlüsseln einiger Daten verwendet wird, können Sie eine der [**Funktionen BCryptImportKeyPair**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptimportkeypair) oder [**NCryptImportKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptimportkey) verwenden. Ein CNG-Anbieter muss das Schlüsselpaar mithilfe eines unterstützten [*Schlüsselblobtyps codieren.*](/windows/desktop/SecGloss/k-gly) [**BCryptExportKey**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptexportkey) kann zum Erstellen des codierten Schlüsselblobs verwendet werden. [CNG-Strukturen](cng-structures.md) beschreibt die wichtigsten BLOB-Typen und -Strukturen, die von Microsoft Key Storage Provider unterstützt werden.

Damit [**BCryptExportKey ein**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptexportkey) persistentes Schlüsselpaar erstellen kann, muss das Eingabeschlüssel-BLOB einen [*privaten Schlüssel enthalten.*](/windows/desktop/SecGloss/p-gly) [*Öffentliche Schlüssel*](/windows/desktop/SecGloss/p-gly) werden nicht beibehalten.

Der Schlüsselname und die Exportrichtlinie sind nicht Teil der [*BLOB-Struktur,*](/windows/desktop/SecGloss/b-gly) die in [CNG-Strukturen definiert ist.](cng-structures.md) Wenn ein BLOB jedoch einen nicht transparenten BLOB-Typ aufweist (z. B. das Speicherbild eines internen Schlüsselzustands), kann das BLOB den Schlüsselnamen und die Exportrichtlinieneigenschaften enthalten.

Im folgenden Verfahren wird beschrieben, wie Sie einen persistenten privaten Schlüssel mit seinen Eigenschaften importieren.

**So importieren Sie einen persistenten Schlüssel**

1.  Erstellen Sie mithilfe der [**NCryptCreatePersistedKey-Funktion**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptcreatepersistedkey) einen persistenten Schlüssel.
2.  Legen Sie mithilfe der [**NCryptSetProperty-Funktion**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptsetproperty) alle gewünschten Eigenschaften für das Schlüsselobjekt fest.
3.  Legen Sie das Blob für den Importschlüssel als Eigenschaft für den Schlüssel fest, und legen Sie den BLOB-Typ als Eigenschaftennamen fest.
4.  Finalisieren Sie den Import des persistenten Schlüssels mithilfe der [**NCryptFinalizeKey-Funktion.**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptfinalizekey)

 

 
