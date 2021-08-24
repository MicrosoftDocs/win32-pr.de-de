---
Description: Im Folgenden werden die Speicherschutzoptionen angezeigt. Sie müssen einen der folgenden Werte angeben, wenn Sie eine Seite im Arbeitsspeicher zuordnen oder schützen. Einem Teil einer Seite können keine Schutzattribute zugewiesen werden. sie können nur einer ganzen Seite zugewiesen werden.
ms.assetid: 09839db7-2118-4a7d-a707-a08c92bd600c
title: Speicherschutzkonstanten (WinNT.h)
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/27/2020
ms.openlocfilehash: 187e8e1f4e137823451771309c9cce19db2e7fbd9c5b57597b51cfc58ca61297
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067690"
---
# <a name="memory-protection-constants"></a>Speicherschutzkonstanten

Im Folgenden werden die Speicherschutzoptionen angezeigt. Sie müssen einen der folgenden Werte angeben, wenn Sie eine Seite im Arbeitsspeicher zuordnen oder schützen. Einem Teil einer Seite können keine Schutzattribute zugewiesen werden. sie können nur einer ganzen Seite zugewiesen werden.

## <a name="example"></a>Beispiel

```cpp
STDMETHODIMP CExtBuffer::FInit
    (
    ULONG cItemMax,     //@parm IN | Maximum number of items ever
    ULONG cbItem,       //@parm IN | Size of each item, in bytes
    ULONG cbPage        //@parm IN | Size of system page size (from SysInfo)
    )
{
    BYTE  *pb;

    m_cbReserved = ((cbItem *cItemMax) / cbPage + 1) *cbPage;
    m_rgItem = (BYTE *) VirtualAlloc( NULL, m_cbReserved, MEM_RESERVE, PAGE_READWRITE );

    if (m_rgItem == NULL)
        return ResultFromScode( E_OUTOFMEMORY );

    m_cbItem  = cbItem;
    m_dbAlloc = (cbItem / cbPage + 1) *cbPage;
    pb = (BYTE *) VirtualAlloc( m_rgItem, m_dbAlloc, MEM_COMMIT, PAGE_READWRITE );
    if (pb == NULL)
        {
        VirtualFree((VOID *) m_rgItem, 0, MEM_RELEASE );
        m_rgItem = NULL;
        return ResultFromScode( E_OUTOFMEMORY );
        }

    m_cbAlloc = m_dbAlloc;
    return ResultFromScode( S_OK );
}
```
Beispiel aus [Windows klassischen Beispielen](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/dataaccess/oledb/sampprov/extbuff.cpp) auf GitHub.

## <a name="constants"></a>Konstanten


| Konstante/Wert                                                                                                                                                                                                                                             | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PAGE_EXECUTE"></span><span id="page_execute"></span><dl> <dt>**SEITE \_ EXECUTE**</dt> <dt>0x10</dt> </dl>                                       | Aktiviert den Ausführungszugriff auf den Bereich von Seiten, für den ein Commit ausgeführt wurde. Ein Versuch, in die Region zu schreiben, für die ein Commit ausgeführt wurde, führt zu einer Zugriffsverletzung.<br/> Dieses Flag wird von der [**CreateFileMapping-Funktion**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) nicht unterstützt.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="PAGE_EXECUTE_READ"></span><span id="page_execute_read"></span><dl> <dt>**SEITE \_ EXECUTE \_ READ**</dt> <dt>0x20</dt> </dl>                       | Aktiviert ausführungs- oder schreibgeschützten Zugriff auf den Bereich von Seiten, für den ein Commit ausgeführt wurde. Ein Versuch, in die Region zu schreiben, für die ein Commit ausgeführt wurde, führt zu einer Zugriffsverletzung.<br/> **Windows Server 2003 und Windows XP:** Dieses Attribut wird von der [**CreateFileMapping-Funktion**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) erst Windows XP mit SP2 und Windows Server 2003 mit SP1 unterstützt.<br/>                                                                                                                                                                                                                                                                                                                                |
| <span id="PAGE_EXECUTE_READWRITE"></span><span id="page_execute_readwrite"></span><dl> <dt>**SEITE \_ EXECUTE \_ READWRITE**</dt> <dt>0x40</dt> </dl>        | Ermöglicht ausführungs-, schreibgeschützten oder Lese-/Schreibzugriff auf den Bereich von Seiten, für den ein Commit ausgeführt wurde.<br/> **Windows Server 2003 und Windows XP:** Dieses Attribut wird von der [**CreateFileMapping-Funktion**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) erst Windows XP mit SP2 und Windows Server 2003 mit SP1 unterstützt.<br/>                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="PAGE_EXECUTE_WRITECOPY"></span><span id="page_execute_writecopy"></span><dl> <dt>**SEITE \_ EXECUTE \_ WRITECOPY**</dt> <dt>0x80</dt> </dl>        | Ermöglicht ausführungs-, schreibgeschützten oder Kopierzugriff auf eine zugeordnete Ansicht eines Dateizuordnungsobjekts. Wenn versucht wird, auf eine Seite mit commiteigen Kopier- und Schreibzugriffen zu schreiben, wird eine private Kopie der Seite erstellt, die für den Prozess erstellt wird. Die private Seite ist als **PAGE \_ EXECUTE \_ READWRITE** markiert, und die Änderung wird auf die neue Seite geschrieben.<br/> Dieses Flag wird von den [**VirtualAlloc-**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) oder [**VirtualAllocEx-Funktionen**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex) nicht unterstützt. **Windows Vista, Windows Server 2003 und Windows XP:** Dieses Attribut wird von der [**CreateFileMapping-Funktion**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) erst Windows Vista mit SP1 und Windows Server 2008 unterstützt.<br/> <br/> |
| <span id="PAGE_NOACCESS"></span><span id="page_noaccess"></span><dl> <dt>**SEITE \_ NOACCESS**</dt> <dt>0x01</dt> </dl>                                    | Deaktiviert den gesamten Zugriff auf den Bereich der Seiten, für den ein Commit ausgeführt wurde. Ein Versuch, aus der Region zu lesen, in die region zu schreiben oder sie auszuführen, führt zu einer Zugriffsverletzung.<br/> Dieses Flag wird von der [**CreateFileMapping-Funktion**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) nicht unterstützt.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="PAGE_READONLY"></span><span id="page_readonly"></span><dl> <dt>**SEITE \_ READONLY-0x02**</dt> <dt></dt> </dl>                                    | Aktiviert den schreibgeschützten Zugriff auf den Bereich von Seiten, für den ein Commit ausgeführt wurde. Ein Versuch, in die Region zu schreiben, für die ein Commit ausgeführt wurde, führt zu einer Zugriffsverletzung. Wenn [die Datenausführungsverhinderung](data-execution-prevention.md) aktiviert ist, führt der Versuch, Code in der Region auszuführen, für die ein Commit ausgeführt wurde, zu einer Zugriffsverletzung.<br/>                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="PAGE_READWRITE"></span><span id="page_readwrite"></span><dl> <dt>**SEITE \_ READWRITE-0x04**</dt> <dt></dt> </dl>                                 | Aktiviert schreibgeschützten Oder Lese-/Schreibzugriff auf den Bereich von Seiten, für den ein Commit ausgeführt wurde. Wenn [die Datenausführungsverhinderung](data-execution-prevention.md) aktiviert ist, führt der Versuch, Code in der Region auszuführen, für die ein Commit ausgeführt wurde, zu einer Zugriffsverletzung.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span id="PAGE_WRITECOPY"></span><span id="page_writecopy"></span><dl> <dt>**SEITE \_ WRITECOPY**</dt> <dt>0x08</dt> </dl>                                 | Aktiviert schreibgeschützten Oder Kopierzugriff auf eine zugeordnete Ansicht eines Dateizuordnungsobjekts. Wenn versucht wird, auf eine Seite mit commiteigen Kopier- und Schreibzugriffen zu schreiben, wird eine private Kopie der Seite erstellt, die für den Prozess erstellt wird. Die private Seite wird als **PAGE \_ READWRITE** markiert, und die Änderung wird auf die neue Seite geschrieben. Wenn [die Datenausführungsverhinderung](data-execution-prevention.md) aktiviert ist, führt der Versuch, Code in der Region auszuführen, für die ein Commit ausgeführt wurde, zu einer Zugriffsverletzung.<br/> Dieses Flag wird von den [**VirtualAlloc-**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) oder [**VirtualAllocEx-Funktionen**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex) nicht unterstützt.<br/>                                                                               |
| <span id="PAGE_TARGETS_INVALID"></span><span id="page_targets_invalid"></span><dl> <dt>**SEITE \_ ZIELE \_ UNGÜLTIGE**</dt> <dt>0x40000000</dt> </dl>        | Legt alle Speicherorte auf den Seiten als ungültige Ziele für CFG fest. Wird zusammen mit jedem Schutz von Ausführungsseiten wie **PAGE \_ EXECUTE,** **PAGE EXECUTE \_ \_ READ,** **PAGE EXECUTE \_ \_ READWRITE** und **PAGE EXECUTE \_ \_ WRITECOPY** verwendet. Jeder indirekte Aufruf von Speicherorten auf diesen Seiten schlägt bei CFG-Überprüfungen fehl, und der Prozess wird beendet. Das Standardverhalten für zugeordnete ausführbare Seiten ist das Kennzeichnen gültiger Aufrufziele für CFG.<br/> Dieses Flag wird von den [**VirtualProtect-**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotect) oder [**CreateFileMapping-Funktionen**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) nicht unterstützt.<br/>                                                                                                              |
| <span id="PAGE_TARGETS_NO_UPDATE"></span><span id="page_targets_no_update"></span><dl> <dt>**SEITE \_ TARGETS \_ NO \_ UPDATE**</dt> <dt>0x40000000</dt> </dl> | Auf Seiten in der Region werden ihre CFG-Informationen nicht aktualisiert, während sich der Schutz für [**VirtualProtect**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotect)ändert. Wenn die Seiten in der Region beispielsweise mit **PAGE \_ TARGETS \_ INVALID** zugeordnet wurden, werden die ungültigen Informationen beibehalten, während sich der Seitenschutz ändert. Dieses Flag ist nur gültig, wenn der Schutz in einen ausführbaren Typ wie **PAGE \_ EXECUTE,** **PAGE EXECUTE \_ \_ READ,** **PAGE EXECUTE \_ \_ READWRITE** und **PAGE EXECUTE \_ \_ WRITECOPY** geändert wird. Das Standardverhalten für **die VirtualProtect-Schutzänderung** in ausführbare Dateien besteht darin, alle Speicherorte als gültige Aufrufziele für CFG zu markieren. <br/>                                           |



Im Folgenden finden Sie Modifizierer, die zusätzlich zu den in der vorherigen Tabelle bereitgestellten Optionen verwendet werden können, sofern nicht anders angegeben.



| Konstante/Wert                                                                                                                                                                                                                       | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PAGE_GUARD"></span><span id="page_guard"></span><dl> <dt>**SEITE \_ GUARD**</dt> <dt>0x100</dt> </dl>                      | Seiten in der Region werden zu Schutzseiten. Jeder Versuch, auf eine Schutzseite zuzugreifen, bewirkt, dass das System eine **STATUS \_ GUARD PAGE \_ \_ VIOLATION-Ausnahme** auslöst und den Status der Schutzseite deaktiviert. Schutzseiten fungieren daher als einmaliger Zugriffsalarm. Weitere Informationen finden Sie unter dem Link zum [Erstellen von Schutzseiten](creating-guard-pages.md).<br/> Wenn ein Zugriffsversuch dazu führt, dass das System den Status der Schutzseite deaktiviert, übernimmt der zugrunde liegende Seitenschutz.<br/> Wenn während eines Systemdiensts eine Wächterseitenausnahme auftritt, gibt der Dienst in der Regel einen Fehlerstatusindikator zurück.<br/> Dieser Wert kann nicht mit **PAGE \_ NOACCESS** verwendet werden.<br/> Dieses Flag wird von der [**CreateFileMapping-Funktion**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) nicht unterstützt.<br/>                                                                                                                                                                                                                              |
| <span id="PAGE_NOCACHE"></span><span id="page_nocache"></span><dl> <dt>**SEITE \_ NOCACHE**</dt> <dt>0x200</dt> </dl>                | Legt fest, dass alle Seiten nicht erreichbar sind. Anwendungen sollten dieses Attribut nur dann verwenden, wenn es explizit für ein Gerät erforderlich ist. Die Verwendung der interlocked-Funktionen mit Arbeitsspeicher, der **SEC \_ NOCACHE** zugeordnet ist, kann zu einer **EXCEPTION ILLEGAL \_ \_ INSTRUCTION-Ausnahme** führen.<br/> Das **PAGE \_ NOCACHE-Flag** kann nicht mit den Flags **PAGE \_ GUARD,** **PAGE \_ NOACCESS** oder **PAGE \_ WRITECOMBINE** verwendet werden.<br/> Das **PAGE \_ NOCACHE-Flag** kann nur verwendet werden, wenn der private Arbeitsspeicher mit den Funktionen [**VirtualAlloc,**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) [**VirtualAllocEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex)oder [**VirtualAllocExNuma**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocexnuma) zugewiesen wird. Um den nicht zwischengespeicherten Speicherzugriff für freigegebenen Arbeitsspeicher zu aktivieren, geben Sie beim Aufrufen der [**CreateFileMapping-Funktion**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) das **SEC \_ NOCACHE-Flag** an.<br/>                                                                                                                                                   |
| <span id="PAGE_WRITECOMBINE"></span><span id="page_writecombine"></span><dl> <dt>**SEITE \_ WRITECOMBINE-0x400**</dt> <dt></dt> </dl> | Legt fest, dass alle Seiten mit Schreibzugriff kombiniert werden sollen. <br/> Anwendungen sollten dieses Attribut nur dann verwenden, wenn es explizit für ein Gerät erforderlich ist. Die Verwendung der interlocked-Funktionen mit Arbeitsspeicher, der als kombinierter Schreibvorgang zugeordnet ist, kann zu einer **EXCEPTION \_ ILLEGAL \_ INSTRUCTION-Ausnahme** führen. <br/> Das **PAGE \_ WRITECOMBINE-Flag** kann nicht mit den Flags **PAGE \_ NOACCESS,** **PAGE \_ GUARD** und **PAGE \_ NOCACHE** angegeben werden. <br/> Das **PAGE \_ WRITECOMBINE-Flag** kann nur verwendet werden, wenn privater Arbeitsspeicher mit den Funktionen [**VirtualAlloc,**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) [**VirtualAllocEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex)oder [**VirtualAllocExNuma**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocexnuma) zugewiesen wird. Geben Sie beim Aufrufen der [**CreateFileMapping-Funktion**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) das **SEC \_ WRITECOMBINE-Flag** an, um den kombinierten Schreibzugriff auf den Arbeitsspeicher für freigegebenen Arbeitsspeicher zu aktivieren.<br/> **Windows Server 2003 und Windows XP:** Dieses Flag wird erst Windows Server 2003 mit SP1 unterstützt.<br/> |



Die folgenden Konstanten können nur mit der [**LoadEnclaveData-Funktion**](/windows/desktop/api/enclaveapi/nf-enclaveapi-loadenclavedata) verwendet werden, wenn Sie eine Enclave mit der Intel Software Guard Extensions(SGX)-Architektur angeben.



| Konstante                                                                                                                                                                                                  | Beschreibung                                                                                                                                 |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PAGE_ENCLAVE_THREAD_CONTROL"></span><span id="page_enclave_thread_control"></span><dl> <dt>**PAGE \_ ENCLAVE \_ THREAD \_ CONTROL**</dt> </dl> | Die Seite enthält eine Threadsteuerelementstruktur (Thread Control Structure, TCS).<br/>                                                                              |
| <span id="PAGE_ENCLAVE_UNVALIDATED"></span><span id="page_enclave_unvalidated"></span><dl> <dt>**PAGE \_ ENCLAVE \_ UNVALIDATED**</dt> </dl>           | Die von Ihnen angegebenen Seiteninhalte werden mit der EEXTEND-Anweisung des Intel SGX-Programmiermodells von der Messung ausgeschlossen.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                   |
| Header<br/>                   | <dl> <dt>WinNT.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga)
</dt> <dt>

[Arbeitsspeicherschutz](memory-protection.md)
</dt> <dt>

[**Virtualalloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc)
</dt> <dt>

[**VirtualAllocEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex)
</dt> <dt>

[**LoadEnclaveData**](/windows/desktop/api/enclaveapi/nf-enclaveapi-loadenclavedata)
</dt> </dl>

 

 
