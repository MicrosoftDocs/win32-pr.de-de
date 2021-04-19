---
description: Sie können symmetrische Schlüssel und asymmetrische Schlüssel mit CNG importieren und exportieren. Und Sie können Schlüssel Export-und-Importfunktionen verwenden, um Schlüssel zwischen Computern zu verschieben.
ms.assetid: 37bda1e0-5dd2-455c-9627-4e7e1b0e04d3
title: Schlüssel Import und-Export
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8be59cc5f5c4b3d1a98fa30cf4e967d5469d2f1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106342630"
---
# <a name="key-import-and-export"></a>Schlüssel Import und-Export

Sie können [*symmetrische Schlüssel*](/windows/desktop/SecGloss/s-gly) und asymmetrische Schlüssel mit CNG importieren und exportieren. Und Sie können Schlüssel Export-und-Importfunktionen verwenden, um Schlüssel zwischen Computern zu verschieben.

## <a name="symmetric-keys"></a>Symmetrische Schlüssel

Zum Importieren oder Exportieren von symmetrischen (oder Sitzungs-) Schlüsseln, in denen derselbe Schlüssel zum Verschlüsseln und Entschlüsseln von Daten verwendet wird, können Sie die Funktionen [**BCryptImportKey**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptimportkey) und [**BCryptExportKey**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptexportkey) verwenden. In der Regel exportieren Sie zuerst einen Schlüssel mithilfe der **BCryptExportKey** -Funktion, bevor Sie mit der **BCryptImportKey** -Funktion importieren. Die Funktionen dienen zum Aktivieren der Verschlüsselung exportierter und importierter Schlüssel mithilfe der Parameter " *hexportkey* " und " *himportkey* ". die Microsoft-Implementierung dieser Funktionen unterstützt jedoch nicht die Verschlüsselung von exportierten und importierten Schlüsseln.

## <a name="asymmetric-keys"></a>Asymmetrische Schlüssel

Wenn Sie asymmetrische (oder [*öffentliche/private*](/windows/desktop/SecGloss/p-gly)) Schlüsselpaare importieren möchten, in denen ein Schlüssel für die Verschlüsselung verwendet wird, und der andere zum Entschlüsseln einiger Daten verwendet wird, können Sie eine der Funktionen [**BCryptImportKeyPair**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptimportkeypair) oder [**ncryptimportkey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptimportkey) verwenden. Ein CNG-Anbieter muss das Schlüsselpaar mit einem unterstützten [*Schlüsselblob*](/windows/desktop/SecGloss/k-gly) -Typ codieren. [**BCryptExportKey**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptexportkey) kann verwendet werden, um das codierte Schlüsselblob zu erstellen. [CNG-Strukturen](cng-structures.md) beschreibt die wichtigsten BLOB-Typen und-Strukturen, die der Microsoft-Schlüsselspeicher Anbieter unterstützt.

Damit [**BCryptExportKey**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptexportkey) ein persistente Schlüsselpaar erstellt, muss das Eingabe Schlüsselblob einen [*privaten Schlüssel*](/windows/desktop/SecGloss/p-gly)enthalten. [*Öffentliche Schlüssel*](/windows/desktop/SecGloss/p-gly) werden nicht persistent gespeichert.

Der Schlüssel Name und die Export Richtlinie sind nicht Teil der in [CNG-Strukturen](cng-structures.md)definierten [*BLOB*](/windows/desktop/SecGloss/b-gly) -Struktur. Wenn ein BLOB jedoch einen nicht transparenten BLOB-Typ aufweist (z. b. das Speicher Image eines internen Schlüssel Zustands), enthält das BLOB möglicherweise den Schlüsselnamen und die Exportrichtlinien Eigenschaften.

Im folgenden Verfahren wird beschrieben, wie ein persistenter privater Schlüssel mit seinen Eigenschaften importiert wird.

**So importieren Sie einen persistenten Schlüssel**

1.  Erstellen Sie einen persistenten Schlüssel mithilfe der [**ncryptkreatepersistedkey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptcreatepersistedkey) -Funktion.
2.  Legen Sie mit der [**ncryptsetproperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptsetproperty) -Funktion alle gewünschten Eigenschaften für das Schlüsselobjekt fest.
3.  Legen Sie das Import-Schlüsselblob als Eigenschaft für den Schlüssel fest, wobei der BLOB-Typ der Eigenschaftsname ist.
4.  Finalisieren Sie den persistenten Schlüssel Import mithilfe der [**ncryptfinalizekey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptfinalizekey) -Funktion.

 

 
