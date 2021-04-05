---
description: Die Datei Zuordnung kann verwendet werden, um eine Datei oder einen Arbeitsspeicher zwischen zwei oder mehr Prozessen freizugeben. Zum Freigeben einer Datei oder eines Speichers müssen alle Prozesse den Namen oder das Handle desselben Datei Zuordnungsobjekts verwenden.
ms.assetid: 942cb50d-df07-444f-bba5-58194556ae66
title: Freigeben von Dateien und Arbeitsspeicher
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98d402eba3f87f1f799593ae0d6b23fba06124a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751728"
---
# <a name="sharing-files-and-memory"></a>Freigeben von Dateien und Arbeitsspeicher

Die Datei Zuordnung kann verwendet werden, um eine Datei oder einen Arbeitsspeicher zwischen zwei oder mehr Prozessen freizugeben. Zum Freigeben einer Datei oder eines Speichers müssen alle Prozesse den Namen oder das Handle desselben Datei Zuordnungsobjekts verwenden.

Zum Freigeben einer Datei erstellt oder öffnet der erste Prozess eine Datei mit [**der Funktion "**](/windows/win32/api/fileapi/nf-fileapi-createfilea) -Funktion". Anschließend wird mithilfe der Funktion "Funktion erstellen" ein Datei Zuordnung Objekt erstellt [**, das das**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) Datei Handle und einen Namen für das Datei-Mapping-Objekt angibt. Die Namen von Ereignis-, Semaphore-, Mutex-, wanutzbaren Timer-, Auftrags-und Datei Zuordnungsobjekten verwenden denselben Namespace. Daher schlagen die Funktionen " **linatefilemapping** " und " [**OpenFileMapping**](/windows/desktop/api/WinBase/nf-winbase-openfilemappinga) " fehl, wenn Sie einen Namen angeben, der von einem Objekt eines anderen Typs verwendet wird.

Um Arbeitsspeicher freizugeben, der nicht mit einer Datei verknüpft ist, muss ein Prozess die Funktion " [**deatefilemapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) " verwenden und \_ anstelle eines vorhandenen Datei Handles einen ungültigen Handle- \_ Wert als *hFile* -Parameter angeben. Das entsprechende Datei Zuordnungsobjekt greift auf den Speicher zu, der von der Auslagerungs Datei des Systems Sie müssen eine Größe angeben, die größer als 0 (null) ist, wenn Sie eine *hFile* mit einem ungültigen \_ handle- \_ Wert in einem aufzurufenden aufzurufen. 

Die einfachste Möglichkeit für andere Prozesse, ein Handle des vom ersten Prozess erstellten Datei Mapping-Objekts abzurufen, besteht in der Verwendung der [**OpenFileMapping**](/windows/desktop/api/WinBase/nf-winbase-openfilemappinga) -Funktion und dem Angeben des Objekt namens. Dies wird als *benannter gemeinsamer Speicher* bezeichnet. Wenn das Datei Zuordnungsobjekt keinen Namen hat, muss der Prozess durch Vererbung oder Duplizierung ein Handle dafür erhalten. Weitere Informationen zur Vererbung und Duplizierung finden Sie unter [Vererbung](../procthread/inheritance.md).

Prozesse, die Dateien oder Arbeitsspeicher freigeben, müssen mithilfe der [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) -oder [**MapViewOfFileEx**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffileex) -Funktion Datei Ansichten erstellen. Sie müssen Ihren Zugriff mithilfe von Semaphoren, Mutexen, Ereignissen oder anderen gegenseitigen Ausschluss Techniken koordinieren. Weitere Informationen finden Sie unter [Synchronisierung](../sync/synchronization.md).

Ein frei gegebenes Datei Zuordnungs Objekt wird erst zerstört, wenn alle Prozesse, von denen es verwendet wird, ihre Handles mithilfe der [**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle) -Funktion für dieses Objekt schließen.

Weitere Informationen zur Datei zuordnungsobjektsicherheit finden Sie unter [Datei Zuordnung Sicherheit und Zugriffsrechte](file-mapping-security-and-access-rights.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen von benanntem Shared Memory](creating-named-shared-memory.md)
</dt> </dl>

 

 
